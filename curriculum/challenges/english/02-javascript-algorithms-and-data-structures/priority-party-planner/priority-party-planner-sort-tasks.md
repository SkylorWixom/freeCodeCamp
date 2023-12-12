---
id: 6577c6561c096764b6139e83
title: sort-tasks
challengeType: 1
dashedName: priority-party-planner-sort-tasks
---

# --description--

Now that you can count tasks in the Priority Party Planner, let's move on to sorting them. In this step, you'll modify your 'planPartyTasks' function to sort tasks based on their priority. Remember, a lower priority number means the task is more urgent.

Your updated function should still accept an array of task objects, each with properties: 'id', 'priority', and 'duration'.

```json
Example task object:
{
  "id": "task1",
  "priority": 1,
  "duration": 30
}
```

# --instructions--

Modify the 'planPartyTasks' function to return the tasks sorted by priority in ascending order. If two tasks have the same priority, sort them by their duration.

# --hints--

'planPartyTasks([])' should return an empty array.

```js
assert(Array.isArray(planPartyTasks([])) && planPartyTasks([]).length === 0);
```

'planPartyTasks' should return tasks sorted by priority and duration.

```js
assert.deepEqual(planPartyTasks([{ id: 'task1', priority: 2, duration: 30 }, { id: 'task2', priority: 1, duration: 20 }]), [{ id: 'task2', priority: 1, duration: 20 }, { id: 'task1', priority: 2, duration: 30 }]);
```


# --seed--

```js
function planPartyTasks(tasks) {
  // Write your sorting logic here
}
console.log(planPartyTasks([{ id: 'task1', priority: 2, duration: 30 }, { id: 'task2', priority: 1, duration: 20 }]));
```

# --solutions--

```js
function planPartyTasks(tasks) {
  return tasks.sort((a, b) => a.priority - b.priority || a.duration - b.duration);
}
console.log(planPartyTasks([{ id: 'task1', priority: 2, duration: 30 }, { id: 'task2', priority: 1, duration: 20 }]));
```
