---
slug: /sdk.contractevents.getevents
title: ContractEvents.getEvents() method
hide_title: true
displayed_sidebar: typescript
---

<!-- Do not edit this file. It is automatically generated by API Documenter. -->

## ContractEvents.getEvents() method

Get Events

## Example

```javascript
// The name of the event to get logs for
const eventName = "Transfer";
// Optionally pass in filters to limit the blocks from which events are retrieved
const filters = {
  fromBlock: 0,
  toBlock: 1000000,
};
const events = await contract.events.getEvents(eventName, filters);
console.log(events[0].eventName);
console.log(events[0].data);
```

**Signature:**

```typescript
getEvents<TEvent extends Record<string, any>>(eventName: string, filters?: EventQueryFilter): Promise<ContractEvent<TEvent>[]>;
```

## Parameters

| Parameter | Type                                          | Description                                                                                        |
| --------- | --------------------------------------------- | -------------------------------------------------------------------------------------------------- |
| eventName | string                                        | The name of the event to get logs for                                                              |
| filters   | [EventQueryFilter](./sdk.eventqueryfilter.md) | <i>(Optional)</i> Specify the from and to block numbers to get events for, defaults to all blocks. |

**Returns:**

Promise&lt;[ContractEvent](./sdk.contractevent.md)&lt;TEvent&gt;\[\]&gt;

The requested event objects with event data

## Remarks

Get a list of the events of a specific type emitted from this contract during the specified time period
