# Duck Typing
To display records together, they probably should have something in common, which I will call their intersection. However, records might also have additional data that ought to be included in the display, which I will call their extersection. If many records have the same extersection, they ought to be cast into a subclass of the intersection which is prepared to visualize the extersection. This automatic casting as subclasses is what I want to achieve with duck typing.

For example, imagine records like:

```json
[
    {"name":"skull"},
    {"name":"teeth","count":11},
    {"name":"ribs","count":6},
    {"name":"femur"}
]
```
In this circumstance, each record has a name, and some records have a count. Displaying these as cards on a UI, some of the records ought to get displayed with 'count'. I'm imagining something like:

```typescript
interface Artifact {
    name: string;
}

interface ArtifactGroup extends Artifact {
    count: number
}
```
Then, I could imagine something like:

```typescript
maxCast<Artifact>({"name":"skull", "count":11}) // Returned type is ArtifactGroup
```

Restricting this to interfaces is probably not the right call. I'd really like something where a class describes a particular query which rests on some data existing (the intersection), then there are subclasses which match particular extersections; each class would function as (eg) a React component, and each would render all their relevant content.