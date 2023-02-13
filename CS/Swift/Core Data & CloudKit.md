![Diagram showing that a persistent container instance contains references to a a managed object model, a managed object context, and a persistent store coordinator that connects to your app's stores.](https://docs-assets.developer.apple.com/published/b9401cae6e/CD-Stack@2x.png)

CloudKit enforces certain limitations on entity attributes. [see here](https://www.hackingwithswift.com/forums/swiftui/default-values-cloudkit-and-coredata/5411/5426) [related SO question](https://stackoverflow.com/questions/56572998/cloudkit-and-coredata-default-values)
- Non-optional attributes must have default values
- One-to-many relationships must be _unordered_

| | Core Data | CloudKit |
|-|-|-|
| Objects | NSManagedObject | CKRecord |
| Models | NSManagedObjectModel | Schema |
| Stores | NSPersistentStore | CKRecordZone / CKDatabase |
