# CoreDataStack
CoreDataStack is a class that manages the setup of a core data stack and also manages two managed object conexts, the private queue context and the main queue context.

## Usage
CoreDataStack is setup as a singleton so the first call to the singleton instance will setup the stack

```swift
  // Returns the singleton instance of the core data stack
  CoreDataStack.defaultStack
```

Any work on the private queue context will automaitically propagate to the main queue context after save and vice versa

```swift
  // Returns the main queue context
  CoreDataStack.defaultStack.mainQueueContext

  // Returns the private queue context
  CoreDataStack.defaultStack.privateQueueContext
```
