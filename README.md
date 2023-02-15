# using_dispatch_work_item_enable_cancellation

Using dispatch work items you can easily cancel a delayed asynchronous GCD task if you no longer need it:

```swift
let workItem = DispatchWorkItem {
    // Your async code goes in here
}

// Execute the work item after 1 second
DispatchQueue.main.asyncAfter(deadline: .now() + 1, execute: workItem)

// You can cancel the work item if you no longer need it
workItem.cancel()
```
