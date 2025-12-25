# Refactoring Guide for LLM Agents

> A comprehensive guide for LLM agents to understand and apply refactoring techniques, based on Martin Fowler's "Refactoring: Improving the Design of Existing Code"

---

## Table of Contents

1. [What is Refactoring?](#1-what-is-refactoring)
2. [Core Principles](#2-core-principles)
3. [Code Smells - When to Refactor](#3-code-smells---when-to-refactor)
4. [Refactoring Catalog](#4-refactoring-catalog)
5. [Testing and Refactoring](#5-testing-and-refactoring)
6. [Agent-Specific Guidelines](#6-agent-specific-guidelines)
7. [Quick Reference](#7-quick-reference)

---

## 1. What is Refactoring?

### Definition

**Refactoring (noun):** A change made to the internal structure of software to make it easier to understand and cheaper to modify **without changing its observable behavior**.

**Refactor (verb):** To restructure software by applying a series of refactorings without changing its observable behavior.

### Key Principles

1. **Behavior Preservation** - The software must function identically before and after refactoring
2. **Small Steps** - Make tiny changes, test frequently
3. **Two Hats Metaphor** - Alternate between "adding features" and "refactoring" - never do both at once

### Why Refactor?

| Benefit | Description |
|---------|-------------|
| **Improves Design** | Prevents code decay, eliminates duplication |
| **Easier to Understand** | Makes code communicate its purpose |
| **Helps Find Bugs** | Clarifying code reveals hidden issues |
| **Faster Development** | Good design enables rapid feature addition |

---

## 2. Core Principles

### The Rhythm of Refactoring

```
Test -> Small Change -> Test -> Small Change -> Test -> Small Change
```

**CRITICAL:** Never skip testing between changes. This rhythm allows refactoring to move quickly and safely.

### The Rule of Three

> "The first time you do something, you just do it. The second time you do something similar, you wince at the duplication, but you do the duplicate thing anyway. The third time you do something similar, you refactor."

**Three strikes and you refactor.**

### When to Refactor

| Situation | Action |
|-----------|--------|
| Adding a feature | Refactor first if design doesn't support the change easily |
| Fixing a bug | Refactor to understand the code better |
| Code review | Refactor as you review to implement suggestions |
| Understanding code | Refactor to clarify what unfamiliar code does |

### When NOT to Refactor

- When code doesn't work at all (rewrite instead)
- Very close to a deadline (technical debt)
- When you should be rewriting from scratch

### Technical Debt Metaphor

Unfinished refactoring = debt. You pay interest through the extra cost of maintenance. Manage your debt by paying it off through refactoring.

---

## 3. Code Smells - When to Refactor

Code smells are indicators that suggest refactoring opportunities. Learn to recognize these patterns.

### 3.1 Duplicated Code

**The #1 smell.** Same code structure in multiple places.

| Location | Refactoring |
|----------|-------------|
| Same class, two methods | Extract Method |
| Sibling subclasses | Extract Method + Pull Up Field |
| Unrelated classes | Extract Class |

### 3.2 Long Method

Short methods are better. Extract when you feel the need to comment.

**Signals:**
- Need to comment what a block does
- Lots of parameters and temp variables
- Complex conditional logic
- Loops with bodies

**Refactorings:**
- Extract Method (99% of cases)
- Replace Temp with Query
- Replace Method with Method Object
- Decompose Conditional

### 3.3 Large Class

Too many instance variables = duplicated code incoming.

**Refactorings:**
- Extract Class
- Extract Subclass
- Extract Interface

### 3.4 Long Parameter List

Objects reduce the need for long parameter lists.

**Refactorings:**
- Replace Parameter with Method
- Preserve Whole Object
- Introduce Parameter Object

### 3.5 Divergent Change

One class changed in different ways for different reasons.

**Example:** "I change these 3 methods for database changes, these 4 for new financial instruments"

**Refactoring:** Extract Class - separate the concerns

### 3.6 Shotgun Surgery

One change requires editing many classes.

**Refactorings:**
- Move Method
- Move Field
- Inline Class

### 3.7 Feature Envy

A method uses more features of another class than its own.

**Refactorings:**
- Move Method
- Extract Method + Move Method

### 3.8 Data Clumps

Same data items appearing together repeatedly.

**Refactorings:**
- Extract Class
- Introduce Parameter Object
- Preserve Whole Object

### 3.9 Primitive Obsession

Using primitives instead of small objects for simple tasks.

**Refactorings:**
- Replace Data Value with Object
- Replace Type Code with Class
- Replace Type Code with Subclasses
- Replace Type Code with State/Strategy

### 3.10 Switch Statements

Switch statements often indicate need for polymorphism.

**Refactorings:**
- Replace Type Code with Subclasses
- Replace Type Code with State/Strategy
- Replace Conditional with Polymorphism
- Replace Parameter with Explicit Methods

### 3.11 Parallel Inheritance Hierarchies

Creating a subclass in one hierarchy requires creating one in another.

**Refactorings:**
- Move Method
- Move Field

### 3.12 Lazy Class

A class not doing enough to justify its existence.

**Refactorings:**
- Collapse Hierarchy
- Inline Class

### 3.13 Speculative Generality

"We might need this someday" hooks that aren't used.

**Refactorings:**
- Collapse Hierarchy
- Inline Class
- Remove Parameter
- Rename Method

### 3.14 Temporary Field

Instance variables set only in certain circumstances.

**Refactorings:**
- Extract Class
- Introduce Null Object

### 3.15 Message Chains

Long chains: `a.getB().getC().getD().doSomething()`

**Refactorings:**
- Hide Delegate
- Extract Method + Move Method

### 3.16 Middle Man

A class that delegates most of its work.

**Refactorings:**
- Remove Middle Man
- Inline Method
- Replace Delegation with Inheritance

### 3.17 Inappropriate Intimacy

Classes too involved in each other's private details.

**Refactorings:**
- Move Method
- Move Field
- Change Bidirectional to Unidirectional
- Extract Class
- Hide Delegate
- Replace Inheritance with Delegation

### 3.18 Data Class

Classes with only fields and getters/setters.

**Refactorings:**
- Encapsulate Field
- Encapsulate Collection
- Remove Setting Method
- Move Method
- Extract Method

### 3.19 Refused Bequest

Subclass doesn't use inherited methods/data.

**Refactorings:**
- Push Down Method
- Push Down Field
- Replace Inheritance with Delegation

### 3.20 Comments as Deodorant

Comments hiding bad code instead of explaining why.

**Refactorings:**
- Extract Method
- Rename Method
- Introduce Assertion

> "When you feel the need to write a comment, first try to refactor the code so that any comment becomes superfluous."

---

## 4. Refactoring Catalog

### 4.1 Composing Methods

#### Extract Method

**Situation:** Code fragment that can be grouped together.

**Mechanics:**
1. Create new method named after intention (what, not how)
2. Copy extracted code to new method
3. Handle local variables (parameters, temps, return values)
4. Replace original code with method call
5. Compile and test

```java
// Before
void printOwing() {
    // print banner
    System.out.println("**************************");
    System.out.println("***** Customer Owes ******");
    System.out.println("**************************");

    // print details
    System.out.println("name:" + _name);
    System.out.println("amount" + _outstanding);
}

// After
void printOwing() {
    printBanner();
    printDetails();
}

void printBanner() {
    System.out.println("**************************");
    System.out.println("***** Customer Owes ******");
    System.out.println("**************************");
}

void printDetails() {
    System.out.println("name:" + _name);
    System.out.println("amount" + _outstanding);
}
```

#### Inline Method

**Situation:** Method body is as clear as its name.

```java
// Before
int getRating() {
    return moreThanFiveLateDeliveries() ? 2 : 1;
}
boolean moreThanFiveLateDeliveries() {
    return _numberOfLateDeliveries > 5;
}

// After
int getRating() {
    return (_numberOfLateDeliveries > 5) ? 2 : 1;
}
```

#### Replace Temp with Query

**Situation:** Temporary variable holds result of an expression.

```java
// Before
double getPrice() {
    int basePrice = _quantity * _itemPrice;
    if (basePrice > 1000)
        return basePrice * 0.95;
    else
        return basePrice * 0.98;
}

// After
double getPrice() {
    if (basePrice() > 1000)
        return basePrice() * 0.95;
    else
        return basePrice() * 0.98;
}

double basePrice() {
    return _quantity * _itemPrice;
}
```

#### Introduce Explaining Variable

**Situation:** Complicated expression needs clarification.

```java
// Before
if ((platform.toUpperCase().indexOf("MAC") > -1) &&
    (browser.toUpperCase().indexOf("IE") > -1) &&
    wasInitialized() && resize > 0) {
    // do something
}

// After
final boolean isMacOs = platform.toUpperCase().indexOf("MAC") > -1;
final boolean isIEBrowser = browser.toUpperCase().indexOf("IE") > -1;
final boolean wasResized = resize > 0;

if (isMacOs && isIEBrowser && wasInitialized() && wasResized) {
    // do something
}
```

#### Split Temporary Variable

**Situation:** Temp assigned more than once (not loop/collecting variable).

```java
// Before
double temp = 2 * (_height + _width);
System.out.println(temp);
temp = _height * _width;
System.out.println(temp);

// After
final double perimeter = 2 * (_height + _width);
System.out.println(perimeter);
final double area = _height * _width;
System.out.println(area);
```

#### Remove Assignments to Parameters

**Situation:** Code assigns to a parameter.

```java
// Before
int discount(int inputVal, int quantity, int yearToDate) {
    if (inputVal > 50) inputVal -= 2;
    // ...
}

// After
int discount(int inputVal, int quantity, int yearToDate) {
    int result = inputVal;
    if (inputVal > 50) result -= 2;
    // ...
}
```

#### Replace Method with Method Object

**Situation:** Long method with too many local variables to extract.

```java
// Before
class Order {
    double price() {
        double primaryBasePrice;
        double secondaryBasePrice;
        double tertiaryBasePrice;
        // long computation...
    }
}

// After
class Order {
    double price() {
        return new PriceCalculator(this).compute();
    }
}

class PriceCalculator {
    private double primaryBasePrice;
    private double secondaryBasePrice;
    private double tertiaryBasePrice;

    double compute() {
        // now can extract freely
    }
}
```

#### Substitute Algorithm

**Situation:** Want to replace algorithm with a clearer one.

```java
// Before
String foundPerson(String[] people) {
    for (int i = 0; i < people.length; i++) {
        if (people[i].equals("Don")) return "Don";
        if (people[i].equals("John")) return "John";
        if (people[i].equals("Kent")) return "Kent";
    }
    return "";
}

// After
String foundPerson(String[] people) {
    List candidates = Arrays.asList(new String[]{"Don", "John", "Kent"});
    for (int i = 0; i < people.length; i++) {
        if (candidates.contains(people[i]))
            return people[i];
    }
    return "";
}
```

### 4.2 Moving Features Between Objects

#### Move Method

**Situation:** Method uses more features of another class.

**Mechanics:**
1. Examine features used - consider moving them too
2. Check for polymorphism in hierarchy
3. Declare method in target class
4. Copy and adapt code
5. Turn source into delegation or remove
6. Compile and test

#### Move Field

**Situation:** Field used more by another class.

**Mechanics:**
1. Encapsulate field if public
2. Create field with accessors in target
3. Determine how to reference target from source
4. Remove field from source
5. Replace all references
6. Compile and test

#### Extract Class

**Situation:** One class doing work that should be two.

```java
// Before
class Person {
    private String _name;
    private String _officeAreaCode;
    private String _officeNumber;

    String getTelephoneNumber() {
        return "(" + _officeAreaCode + ") " + _officeNumber;
    }
}

// After
class Person {
    private String _name;
    private TelephoneNumber _officeTelephone;

    String getTelephoneNumber() {
        return _officeTelephone.getTelephoneNumber();
    }
}

class TelephoneNumber {
    private String _areaCode;
    private String _number;

    String getTelephoneNumber() {
        return "(" + _areaCode + ") " + _number;
    }
}
```

#### Inline Class

**Situation:** Class isn't doing much.

Reverse of Extract Class - fold class into another.

#### Hide Delegate

**Situation:** Client calls delegate class of an object.

```java
// Before
manager = john.getDepartment().getManager();

// After
manager = john.getManager();

// In Person class
public Person getManager() {
    return _department.getManager();
}
```

#### Remove Middle Man

**Situation:** Class doing too much simple delegation.

Reverse of Hide Delegate - let client call delegate directly.

#### Introduce Foreign Method

**Situation:** Server class needs method you can't add.

```java
// Before
Date newStart = new Date(previousEnd.getYear(),
    previousEnd.getMonth(), previousEnd.getDate() + 1);

// After
Date newStart = nextDay(previousEnd);

private static Date nextDay(Date arg) {
    // foreign method, should be on Date
    return new Date(arg.getYear(), arg.getMonth(), arg.getDate() + 1);
}
```

#### Introduce Local Extension

**Situation:** Server class needs several methods you can't add.

Create subclass or wrapper with the extra methods.

### 4.3 Organizing Data

#### Self Encapsulate Field

**Situation:** Direct field access becoming awkward.

```java
// Before
private int _low, _high;
boolean includes(int arg) {
    return arg >= _low && arg <= _high;
}

// After
private int _low, _high;
boolean includes(int arg) {
    return arg >= getLow() && arg <= getHigh();
}
int getLow() { return _low; }
int getHigh() { return _high; }
```

#### Replace Data Value with Object

**Situation:** Data item needs additional data or behavior.

```java
// Before
class Order {
    private String _customer;
}

// After
class Order {
    private Customer _customer;
}

class Customer {
    private String _name;
}
```

#### Replace Array with Object

**Situation:** Array where elements mean different things.

```java
// Before
String[] row = new String[3];
row[0] = "Liverpool";
row[1] = "15";

// After
Performance row = new Performance();
row.setName("Liverpool");
row.setWins("15");
```

#### Replace Magic Number with Symbolic Constant

```java
// Before
double potentialEnergy(double mass, double height) {
    return mass * 9.81 * height;
}

// After
static final double GRAVITATIONAL_CONSTANT = 9.81;

double potentialEnergy(double mass, double height) {
    return mass * GRAVITATIONAL_CONSTANT * height;
}
```

#### Encapsulate Field

**Situation:** Public field exists.

```java
// Before
public String _name;

// After
private String _name;
public String getName() { return _name; }
public void setName(String arg) { _name = arg; }
```

#### Encapsulate Collection

**Situation:** Method returns a collection.

Return read-only view; provide add/remove methods.

#### Replace Type Code with Class

**Situation:** Class has numeric type code that doesn't affect behavior.

```java
// Before
class Person {
    public static final int O = 0;
    public static final int A = 1;
    public static final int B = 2;
    public static final int AB = 3;
    private int _bloodGroup;
}

// After
class Person {
    private BloodGroup _bloodGroup;
}

class BloodGroup {
    public static final BloodGroup O = new BloodGroup(0);
    public static final BloodGroup A = new BloodGroup(1);
    // ...
}
```

#### Replace Type Code with Subclasses

**Situation:** Immutable type code affects class behavior.

```java
// Before
class Employee {
    private int _type;
    static final int ENGINEER = 0;
    static final int SALESMAN = 1;
}

// After
abstract class Employee {}
class Engineer extends Employee {}
class Salesman extends Employee {}
```

#### Replace Type Code with State/Strategy

**Situation:** Type code affects behavior but can't use subclassing.

Use State or Strategy pattern to replace the type code.

#### Replace Conditional with Polymorphism

**Situation:** Conditional that chooses behavior based on type.

```java
// Before
double getSpeed() {
    switch (_type) {
        case EUROPEAN: return getBaseSpeed();
        case AFRICAN: return getBaseSpeed() - getLoadFactor();
        case NORWEGIAN_BLUE: return isNailed ? 0 : getBaseSpeed();
    }
}

// After
class European extends Bird {
    double getSpeed() { return getBaseSpeed(); }
}
class African extends Bird {
    double getSpeed() { return getBaseSpeed() - getLoadFactor(); }
}
class NorwegianBlue extends Bird {
    double getSpeed() { return isNailed ? 0 : getBaseSpeed(); }
}
```

### 4.4 Simplifying Conditional Expressions

#### Decompose Conditional

**Situation:** Complicated conditional.

```java
// Before
if (date.before(SUMMER_START) || date.after(SUMMER_END))
    charge = quantity * _winterRate + _winterServiceCharge;
else
    charge = quantity * _summerRate;

// After
if (notSummer(date))
    charge = winterCharge(quantity);
else
    charge = summerCharge(quantity);
```

#### Consolidate Conditional Expression

**Situation:** Sequence of conditionals with same result.

```java
// Before
double disabilityAmount() {
    if (_seniority < 2) return 0;
    if (_monthsDisabled > 12) return 0;
    if (_isPartTime) return 0;
    // compute disability amount
}

// After
double disabilityAmount() {
    if (isNotEligibleForDisability()) return 0;
    // compute disability amount
}
```

#### Consolidate Duplicate Conditional Fragments

**Situation:** Same code in all branches of conditional.

```java
// Before
if (isSpecialDeal()) {
    total = price * 0.95;
    send();
} else {
    total = price * 0.98;
    send();
}

// After
if (isSpecialDeal())
    total = price * 0.95;
else
    total = price * 0.98;
send();
```

#### Remove Control Flag

**Situation:** Variable acting as control flag for loop.

Replace with `break` or `return`.

#### Replace Nested Conditional with Guard Clauses

**Situation:** Method has conditional that doesn't make clear the normal path.

```java
// Before
double getPayAmount() {
    double result;
    if (_isDead) result = deadAmount();
    else {
        if (_isSeparated) result = separatedAmount();
        else {
            if (_isRetired) result = retiredAmount();
            else result = normalPayAmount();
        }
    }
    return result;
}

// After
double getPayAmount() {
    if (_isDead) return deadAmount();
    if (_isSeparated) return separatedAmount();
    if (_isRetired) return retiredAmount();
    return normalPayAmount();
}
```

#### Introduce Null Object

**Situation:** Repeated null checks.

```java
// Before
if (customer == null) plan = BillingPlan.basic();
else plan = customer.getPlan();

// After (with NullCustomer class)
plan = customer.getPlan();

class NullCustomer extends Customer {
    Plan getPlan() { return BillingPlan.basic(); }
}
```

#### Introduce Assertion

**Situation:** Code assumes something about state.

```java
// Before
double getExpenseLimit() {
    // should have either expense limit or primary project
    return (_expenseLimit != NULL_EXPENSE) ?
        _expenseLimit : _primaryProject.getMemberExpenseLimit();
}

// After
double getExpenseLimit() {
    assert (_expenseLimit != NULL_EXPENSE || _primaryProject != null);
    return (_expenseLimit != NULL_EXPENSE) ?
        _expenseLimit : _primaryProject.getMemberExpenseLimit();
}
```

### 4.5 Making Method Calls Simpler

#### Rename Method

**Situation:** Method name doesn't reveal purpose.

#### Add Parameter / Remove Parameter

Add when method needs more info; remove when parameter isn't used.

#### Separate Query from Modifier

**Situation:** Method returns value and changes state.

Split into two methods: one that returns, one that modifies.

#### Parameterize Method

**Situation:** Several methods do similar things with different values.

```java
// Before
void fivePercentRaise() { ... }
void tenPercentRaise() { ... }

// After
void raise(double percentage) { ... }
```

#### Replace Parameter with Explicit Methods

**Situation:** Method runs different code based on enum parameter.

```java
// Before
void setValue(String name, int value) {
    if (name.equals("height")) _height = value;
    if (name.equals("width")) _width = value;
}

// After
void setHeight(int value) { _height = value; }
void setWidth(int value) { _width = value; }
```

#### Preserve Whole Object

**Situation:** Getting values from object to pass as parameters.

```java
// Before
int low = daysTempRange.getLow();
int high = daysTempRange.getHigh();
withinPlan = plan.withinRange(low, high);

// After
withinPlan = plan.withinRange(daysTempRange);
```

#### Replace Parameter with Method

**Situation:** Object can get value itself instead of receiving it.

```java
// Before
int basePrice = _quantity * _itemPrice;
discountLevel = getDiscountLevel();
double finalPrice = discountedPrice(basePrice, discountLevel);

// After
int basePrice = _quantity * _itemPrice;
double finalPrice = discountedPrice(basePrice);
```

#### Introduce Parameter Object

**Situation:** Group of parameters that go together.

```java
// Before
amountInvoiced(Date start, Date end)
amountReceived(Date start, Date end)
amountOverdue(Date start, Date end)

// After
amountInvoiced(DateRange range)
amountReceived(DateRange range)
amountOverdue(DateRange range)
```

#### Hide Method

**Situation:** Method not used by other classes.

Make it private.

#### Replace Constructor with Factory Method

**Situation:** Want more than simple construction.

```java
// Before
Employee eng = new Employee(ENGINEER);

// After
Employee eng = Employee.create(ENGINEER);
// or
Employee eng = Engineer.create();
```

#### Replace Error Code with Exception

**Situation:** Method returns special code for errors.

Throw exception instead.

#### Replace Exception with Test

**Situation:** Throwing exception for condition caller could check.

```java
// Before
double getValueForPeriod(int periodNumber) {
    try {
        return _values[periodNumber];
    } catch (ArrayIndexOutOfBoundsException e) {
        return 0;
    }
}

// After
double getValueForPeriod(int periodNumber) {
    if (periodNumber >= _values.length) return 0;
    return _values[periodNumber];
}
```

### 4.6 Dealing with Generalization

#### Pull Up Field / Push Down Field

Move fields up to superclass or down to subclass as appropriate.

#### Pull Up Method / Push Down Method

Move methods up to superclass or down to subclass as appropriate.

#### Pull Up Constructor Body

**Situation:** Subclass constructors have identical bodies.

```java
// Before
class Manager extends Employee {
    Manager(String name, String id, int grade) {
        _name = name;
        _id = id;
        _grade = grade;
    }
}

// After
class Manager extends Employee {
    Manager(String name, String id, int grade) {
        super(name, id);
        _grade = grade;
    }
}
```

#### Extract Subclass

**Situation:** Class has features used only by some instances.

#### Extract Superclass

**Situation:** Two classes have similar features.

#### Extract Interface

**Situation:** Multiple clients use same subset of class interface.

#### Collapse Hierarchy

**Situation:** Superclass and subclass aren't very different.

Merge them.

#### Form Template Method

**Situation:** Subclasses have methods with similar steps in same order.

Put steps in superclass, call abstract methods for differences.

#### Replace Inheritance with Delegation

**Situation:** Subclass uses only part of superclass interface.

```java
// Before
class MyStack extends Vector { ... }

// After
class MyStack {
    private Vector _vector = new Vector();
}
```

#### Replace Delegation with Inheritance

**Situation:** Using delegation and delegating all methods.

Make delegating class a subclass instead.

---

## 5. Testing and Refactoring

### The Essential Precondition

> **"If you want to refactor, the essential precondition is having solid tests."**

### Self-Testing Code Benefits

- Writing tests speeds up programming
- Tests are powerful bug detectors
- Most debugging time eliminated
- Finding bugs takes minutes, not hours

### Testing Principles

```
Make sure all tests are fully automatic and check their own results.
```

```
Run your tests frequently. Localize tests whenever you compile.
```

```
A suite of tests is a powerful bug detector that decapitates the time it takes to find bugs.
```

### What to Test

- Test areas most worried about going wrong
- Test boundary conditions
- Test for expected exceptions
- Don't try to test everything - test the risky areas

```
It is better to write and run incomplete tests than not to run complete tests.
```

```
Think of the boundary conditions under which things might go wrong.
```

```
Don't forget to test that exceptions are raised when things are expected to go wrong.
```

### Bug Reports

```
When you get a bug report, start by writing a unit test that exposes the bug.
```

---

## 6. Agent-Specific Guidelines

### Before Refactoring

1. **Ensure tests exist** - Don't refactor untested code
2. **Verify tests pass** - Start from a known-good state
3. **Understand the code** - Read before modifying
4. **Identify the smell** - Know what you're fixing

### During Refactoring

1. **Take small steps** - One change at a time
2. **Test after each change** - Verify nothing broke
3. **Commit frequently** - Preserve working states
4. **Don't add features** - Stay focused on structure

### Safe Refactoring Checklist

```markdown
[ ] Tests exist and pass
[ ] I understand what the code does
[ ] I've identified the specific smell
[ ] I'm making one small change
[ ] I'll test before the next change
[ ] I'm not adding new functionality
```

### Common Agent Mistakes to Avoid

| Mistake | Correct Approach |
|---------|------------------|
| Refactoring and adding features together | Separate the activities |
| Making too many changes at once | Small steps, test between |
| Refactoring without tests | Write tests first |
| Guessing what code does | Read and understand first |
| Over-engineering | Keep it simple |
| Premature abstraction | Wait for third occurrence |

### Refactoring Priority for Agents

**High Priority (Fix First):**
1. Duplicated code
2. Long methods
3. Large classes
4. Long parameter lists

**Medium Priority:**
5. Feature envy
6. Data clumps
7. Switch statements
8. Primitive obsession

**Lower Priority (Consider Context):**
9. Speculative generality
10. Message chains
11. Middle man
12. Comments hiding bad code

### Communication Guidelines

When suggesting refactoring to users:

1. **Explain the smell** - What's wrong and why
2. **Propose the refactoring** - What you'll do
3. **Describe the benefit** - Why it's better
4. **Show before/after** - Make it concrete
5. **Preserve behavior** - Reassure nothing breaks

---

## 7. Quick Reference

### Smell to Refactoring Map

| Smell | Primary Refactoring |
|-------|---------------------|
| Duplicated Code | Extract Method, Pull Up Method |
| Long Method | Extract Method |
| Large Class | Extract Class, Extract Subclass |
| Long Parameter List | Introduce Parameter Object |
| Divergent Change | Extract Class |
| Shotgun Surgery | Move Method, Move Field |
| Feature Envy | Move Method |
| Data Clumps | Extract Class |
| Primitive Obsession | Replace Data Value with Object |
| Switch Statements | Replace Conditional with Polymorphism |
| Parallel Inheritance | Move Method, Move Field |
| Lazy Class | Inline Class |
| Speculative Generality | Collapse Hierarchy |
| Temporary Field | Extract Class |
| Message Chains | Hide Delegate |
| Middle Man | Remove Middle Man |
| Inappropriate Intimacy | Move Method, Move Field |
| Data Class | Move Method |
| Refused Bequest | Replace Inheritance with Delegation |
| Comments | Extract Method, Rename Method |

### Refactoring Decision Tree

```
Is the code tested?
├── No → Write tests first
└── Yes → Is there a code smell?
    ├── No → Don't refactor
    └── Yes → What type of smell?
        ├── Duplication → Extract Method
        ├── Long Method → Extract Method
        ├── Wrong Location → Move Method/Field
        ├── Complex Conditional → Decompose Conditional
        └── Type Code → Replace with Polymorphism
```

### The Refactoring Mantra

1. **RED** - Write a failing test
2. **GREEN** - Make it pass (simplest way)
3. **REFACTOR** - Clean up while tests pass

### Key Takeaways

1. Refactoring = changing structure without changing behavior
2. Small steps + frequent tests = safety
3. Code smells guide when to refactor
4. The catalog provides how to refactor
5. Tests are non-negotiable prerequisite
6. Three strikes, then refactor
7. Separate refactoring from feature work

---

## Resources

- **Book:** "Refactoring: Improving the Design of Existing Code" by Martin Fowler
- **Website:** [refactoring.com](https://refactoring.com)
- **Related:** "Design Patterns" by Gang of Four
- **Testing:** JUnit, xUnit frameworks

---

*This guide summarizes Martin Fowler's "Refactoring" for use by LLM agents when analyzing and improving code.*
