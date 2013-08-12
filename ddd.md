

Domain-driven design

<http://en.wikipedia.org/wiki/Domain_driven_design>

Domain objects:

- Entity: An object that is not defined by its attributes, but rather by a thread of continuity and its identity.
- Value Object: An object that contains attributes but has no conceptual identity. They should be treated as immutable.

- Service: When an operation does not conceptually belong to any object. Following the natural contours of the problem, you can implement these operations in services. See also Service (systems architecture).
- Repository: methods for retrieving domain objects should delegate to a specialized Repository object such that alternative storage implementations may be easily interchanged.
- Factory: methods for creating domain objects should delegate to a specialized Factory object such that alternative implementations may be easily interchanged.
