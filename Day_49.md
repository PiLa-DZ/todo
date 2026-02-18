Learn TypeScript
1. Advanced_Types
    1. Mapped_Types ([K in keyof T])
    2. Conditional_Types (T extends  U ? X : Y)
    3. Literal_Types (let a: "admin")
    4. Template_Literal_Types (type Shirt = `${Size}-${Color}-shirt`)
    5. Recursive_Types // A Recursive Type is a type that references itself. 
2. Modules
    1. Modules_Internal_External // Namespaces vs Modules
    2. Namespaces // Namespaces were more common before ES6 modules became the standard
    3. Ambient_Modules (declare module "some-untyped-library")
    4. External_Modules (export | export default | import {a, b} | import * as DB | import type {a}) // Or Re-exporting 
    5. Namespace_Augmentation // "teleport" new properties into libraries you didn't write
    6. Global_Augmentation (declare global)
3. Ecosystem (developer experience (DX))
    1. Formatting (Prettier Extention) // For looks
    2. Linting (ESLint) // For Code Quality & Patterns
    3. Useful_Packages
    4. Build_Tools ( (Compilers/Bundlers) and (Task Runners) )
4. TSConfig
    1. Compiler_Options (Type Checking, Modules, Emit)
    2. include (Tells TS where to look for files)
    3. exclude (Tells TS what to ignore)
5. Module Systems
    1. CommonJS   (CJS) (module.exports, require)
    2. ES Modules (ESM) (export, import)
