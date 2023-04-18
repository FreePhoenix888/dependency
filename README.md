# dependency

# How to use?
```ts
const containTypeLinkId = await deep.id("@deep-foundation/core", "Contain");

const dependantPackageLinkId = ;
const dependencyPackageName = ;
const anyLinkIdFromDependencyPackage = ;

await deep.serial({
  operations: [
    {
      table: 'links',
      type: 'insert',
      objects:
        [
          {
            type_id: await deep.id("@freephoenix888/dependency", "Dependency"),
            from_id: dependantPackageLinkId,
            to_id: anyLinkIdFromDependencyPackage,
            in: {
              data: [
                {
                  type_id: containTypeLinkId,
                  from_id: dependantPackageLinkId,
                  string: {
                    data: {
                      value: `${dependencyPackageName}Dependency`
                    }
                  }
                }
              ]
            },
          }
        ]
    }
  ]
})
```

# Example
```ts
const containTypeLinkId = await deep.id("@deep-foundation/core", "Contain");

const dependantPackageLinkId = await deep.id("@deep-foundation/deep-memo");
const dependencyPackageName = "@deep-foundation/device";
const anyLinkIdFromDependencyPackage = await deep.id(dependencyPackageName, "Device");

await deep.serial({
  operations: [
    {
      table: 'links',
      type: 'insert',
      objects:
        [
          {
            type_id: await deep.id("@freephoenix888/dependency", "Dependency"),
            from_id: dependantPackageLinkId,
            to_id: anyLinkIdFromDependencyPackage,
            in: {
              data: [
                {
                  type_id: containTypeLinkId,
                  from_id: dependantPackageLinkId,
                  string: {
                    data: {
                      value: `${dependencyPackageName}Dependency`
                    }
                  }
                }
              ]
            },
          }
        ]
    }
  ]
})
```
https://www.npmjs.com/package/@deep-foundation/deep-memo/v/0.0.1
