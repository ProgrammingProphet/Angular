# Angular Folder Structure Explained

Angular provides a predefined folder structure that organizes the files and directories within an Angular application. This structure promotes maintainability, scalability, and clarity when developing and managing your application.

In this README, we will explain the purpose of each folder and file in the default Angular project structure and provide insights into how to organize your application efficiently.

---

## Default Angular Project Structure
When you generate a new Angular application using the Angular CLI (`ng new my-app`), the following folder structure is created:

```
my-app
├── e2e
├── node_modules
├── src
│   ├── app
│   ├── assets
│   ├── environments
│   ├── main.ts
│   ├── polyfills.ts
│   ├── styles.scss
│   ├── index.html
│   └── test.ts
├── angular.json
├── package.json
├── tsconfig.json
└── README.md
```

Let’s dive into each folder and its contents:

---

## Root-Level Files

### 1. **angular.json**
- The main configuration file for the Angular CLI.
- Defines build, test, and serve configurations.
- Allows customization of file paths, environments, and optimization settings.

### 2. **package.json**
- Lists the dependencies and devDependencies required for the project.
- Contains scripts for building, testing, and running the application.

### 3. **tsconfig.json**
- TypeScript configuration file.
- Specifies TypeScript compiler options like module resolution, target version, and file inclusion.

### 4. **README.md**
- Provides an overview of the project.
- Useful for documenting project purpose, setup instructions, and usage.

### 5. **node_modules/**
- Contains all the dependencies and modules installed via npm.
- Automatically created by running `npm install`.

---

## `src` Folder
This folder contains the main source code of the application.

### 1. **src/app/**
- The core directory where the application logic resides.
- Contains components, services, modules, pipes, and other features.

#### Example Structure of `src/app/`:
```
app
├── app.component.ts       // Component logic
├── app.component.html     // Component template
├── app.component.scss     // Component styles
├── app.module.ts          // Root module
└── shared/                // Shared components, directives, or services
```

#### Best Practices for `src/app/`:
- Create feature-specific modules (e.g., `user/`, `admin/`).
- Store shared utilities or services in a `shared/` directory.

---

### 2. **src/assets/**
- Used for static assets like images, icons, and fonts.
- These files are served as-is without being processed by Angular.

---

### 3. **src/environments/**
- Contains environment-specific configurations.
- Files like `environment.prod.ts` and `environment.ts` store API URLs and other settings.
- Angular uses the correct file during the build process (e.g., `ng build --prod` for production).

---

### 4. **src/index.html**
- The main HTML file of the application.
- Contains the `<app-root>` tag where the Angular application is bootstrapped.

---

### 5. **src/main.ts**
- The entry point of the application.
- Bootstraps the root module (`AppModule`) to launch the application.

---

### 6. **src/polyfills.ts**
- Includes polyfills for older browsers to support modern JavaScript features.
- Necessary for ensuring cross-browser compatibility.

---

### 7. **src/styles.scss**
- Global styles for the application.
- You can import CSS/SCSS files or define styles for HTML elements here.

---

### 8. **src/test.ts**
- Configures the testing environment.
- Used when running unit tests.

---

## `e2e` Folder
- Contains end-to-end test files.
- Uses Protractor (or other tools) to perform automated UI tests.

---

## Organizing the Folder Structure
For larger applications, follow these tips:

1. **Feature Modules**:
   - Create separate folders for features (e.g., `auth/`, `dashboard/`).

2. **Shared Modules**:
   - Place shared components, pipes, and services in a `shared/` directory.

3. **Core Module**:
   - Use a `core/` module for singleton services, guards, and application-wide logic.

### Example Advanced Folder Structure:
```
src
├── app
│   ├── core
│   │   ├── services
│   │   └── guards
│   ├── shared
│   │   ├── components
│   │   └── pipes
│   ├── auth
│   │   ├── auth.module.ts
│   │   └── login
│   │       ├── login.component.ts
│   │       ├── login.component.html
│   │       └── login.component.scss
│   └── dashboard
├── assets
├── environments
├── index.html
├── main.ts
├── polyfills.ts
└── styles.scss
```

---

Angular’s default folder structure provides a solid foundation for any project. By following best practices and organizing files logically, you can ensure your application remains scalable and maintainable over time.

