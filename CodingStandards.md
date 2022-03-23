# Coding Standards
## What are Coding Standards?
Coding standards are a set of guidelines, best practices, programming styles and conventions that developers follow when writing source code for a project. Using correct coding standards allows for the creation of cleaner, more readable and more manageable code


# Coding Standards

### Why use coding standards?

*"Always code as if the guy who ends up maintaining your code is a violent psychopath who knows where you live - John Woods"*

[Coding standards and naming conventions](https://www.youtube.com/watch?v=3mlWO01OWIo)

- It is important that every person involved in a project is using the same standards to avoid confusion and promote unity and trust
- In the above video, he states that the average coder spends ten hours reading code for every one hour writing code. We hope to greatly reduce this gap by applying good coding standards, with the hope of having a ratio of four hours of reading to one hour of writing
- The fundamental principles of good code is readability, text searching, reusability and consistency, which will benefit of all of our current and future developers

### Coding Standards to follow at Loisel & Keppel Software

#### Case Types
- Consistency is key here. It doesn't matter which format you use as long as it is the same for all cases of that type
- camelCase for function and variable names
- snake_case for Javascript
- Reserved words should be upper case and should not be used for variable names
- Never use 'name' for a variable name. userName of staffName is more preferable
- These names should be relevant to the case that they are being used for. It helps with searching
- Case sensitivity is also very important for searching 


#### Commenting and Layout  
- It is better to avoid comments if possible as updated code may be out of sync with older comments
- Code should speak for itself as much as possible
- If using comments, the coder should have a three inital name and a date beside the initals
- Date format should be dd/mm/yy


#### Indentation  
- 3 spaces should be used
- Lines should be no longer than 60 characters
- Functions should be used at the same spaces eg. for if statment, the 'if' and 'else' should line up together for better readability


#### Exception Handling 
- Use specific exceptions rather than general
- Write clear, meaningful error messages


**Confusing function names:**  

```
    class LimitedCollection {
  let maxNumberOfItems = 4
  var items = [Int]()
  init(items: [Int]) {
    self.items = items    
  }
  func add(_ item: Int) -> Bool {
    if (items.count < maxNumberOfItems) {
      items.append(item)
      return true
    }
    return false
  }
}
let collection = LimitedCollection(items: [1, 2, 3, 4])
if (collection.add(5)) {
  print("Successfully added new item")  
} else {
  print("Cannot add items: collection is full")
}
// => "Cannot add items: collection is full"
```


**Names are more specialized, easier to understand:**  

```
    class LimitedCollection {
  let maxNumberOfItems = 4
  var items = [Int]()
  init(items: [Int]) {
    self.items = items    
  }
  func isFull() -> Bool {
    return items.count >= maxNumberOfItems
  }
  func addIfPossible(_ item: Int) {
    if (items.count < maxNumberOfItems) {
      items.append(item)
    }
  }
}
let collection = LimitedCollection(items: [1, 2, 3, 4])
if (collection.isFull()) {
  print("Cannot add items: collection is full")
} else {
  collection.addIfPossible(5)
  print("Successfully added new item")  
}
// => "Cannot add items: collection is full"
```

### Advantages of using Coding Standards


#### Better quality
- Makes code easier to read and understand
- Increases the efficiency of projects
- Eliminates errors and helps find problems quicker

#### Customer satisfaction
- Ensures that your customers are getting exactly what they asked for
- It changes need to be made, it will be easier to source the problem and fix it
- Makes it easier to work under time pressure as every line of code is easier to read and easier to search for


#### Time Management
- This will help you deliver projects on time and sometimes ahead of schedule, increasing customer satisfaction 
- Getting the work done quickly and efficiently will satisfy other team members, leading to happier, more productive workers


#### Security
- Good coding standards are vital to protect the company from cyber attacks and hacks by making abnormalities easier to identify

#### Affordability
- Reusing code saves the company time and lowers development costs
- Good coding standards across a company has an exponential effect of saving time and increasing productivity
- Better customer satifaction means that customers are more likely to come back, increasing profitability
- Time is money, therefore saving time on projects helps us save money