Learn TypeScript
1. Utility_Types
    1. Partial (data: Partial<User>) // Everything is optional
    2. Pick (Pick<Student, "id" | "firstName" | "lastName">) // I Just want 'id' And 'firstName' And 'lastName'
    3. Omit (Omit<Student, "id" | "createdAt">) // I want everything EXCEPT 'id' And 'createdAt'
    4. Readonly (Readonly<Config>) // Every properties is Readonly
    5. Record (Record<string, Student>) 
    6. Exclude (Exclude<UnionType, ExcludedMembers>) // Eraser for a list of choices
    7. Extract (Extract<UserAction, `${string}_user`>) // Highlighter for a list of choices
    8. Awaited (Awaited<ReturnType<typeof getStudent>>) // dealing with async/await
    9. Parameters (Parameters<typeof createUser>) // takes all arguments and puts them into a Tuple
    10. Non_Nullable (NonNullable<MiddleName>) // filters out null and undefined from any Union Type.
    11. ReturnType (ReturnType<typeof getFormattedUser>) // ReturnType extracts the type of whatever the function gives back
    12. InstanceType (InstanceType<typeof DatabaseConnection>) // InstanceType tells you what a Class produces when you use the new keyword
