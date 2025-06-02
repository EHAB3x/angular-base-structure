# Angular Base Folder Structure

This project is the **base structure with Tailwind CSS and Flowbite integrated**. It follows a modular and scalable folder structure, ideal for medium to large Angular applications.

> **Note:** There are two additional branches available:
> - **base**: The same structure without Tailwind CSS or Flowbite.
> - **tailwind**: The base structure with only Tailwind CSS integrated.

Below is an overview of the main directories and their purposes:

## Root Level

- **angular.json, package.json, tsconfig*.json**: Angular and TypeScript configuration files.
- **README.md**: Project documentation.
- **public/**: Static assets (e.g., favicon).

## Folder Structure

### Root Level

```text
project-root/                  # Project root directory
├── angular.json               # Angular CLI configuration
├── package.json               # Project dependencies and scripts
├── tsconfig*.json             # TypeScript configuration files
├── README.md                  # Project documentation
├── public/                    # Static public assets
│   └── favicon.ico            # Example static asset
└── src/                       # Main source folder
```

### `src/` - Main Source Folder

```text
src/
├── index.html                 # App entry HTML
├── main.ts                    # App bootstrap file
├── styles.scss                # Global styles
├── app/                       # Main application code
├── assets/                    # Static assets for the app
└── environments/              # Environment-specific config files
```

### `app/` - Application Code

```text
app/
├── app.component.*            # Root component files
├── app.config.ts              # App-wide configuration
├── app.routes.ts              # App routing configuration
├── core/                      # Singleton services/utilities (shared app-wide)
├── layouts/                   # Layout components (header, footer, etc.)
├── pages/                     # Feature modules/pages (routed features)
└── shared/                    # Reusable shared components
```

#### `core/` - Core Services and Utilities

```text
core/
├── enums/                     # TypeScript enums
├── guards/                    # Route guards
├── interceptors/              # HTTP interceptors
├── interfaces/                # TypeScript interfaces
├── models/                    # Data models
├── resolvers/                 # Route resolvers
├── services/                  # Core services (API, Auth, etc.)
└── types/                     # Custom types
```

#### `layouts/` - Layout Components

```text
layouts/
├── header/                    # Header layout component
└── footer/                    # Footer layout component
```

#### `pages/` - Feature Modules/Pages

```text
pages/
└── home-page/                 # Example feature page
```

#### `shared/` - Shared Components

```text
shared/
└── loader/                    # Example shared component
```

### `assets/` - Static Assets

```text
assets/
├── fonts/                     # Custom fonts
├── media/                     # Media assets (images, sounds, svgs, videos)
│   ├── images/                # Images
│   ├── sounds/                # Sound files
│   ├── svgs/                  # SVG files
│   └── videos/                # Video files
└── scss/                      # Global SCSS styles
    ├── global/                # Global style rules
    ├── mixin/                 # SCSS mixins
    ├── plugins/               # SCSS plugin styles
    ├── shared/                # Shared style rules
    └── variables/             # SCSS variables (colors, breakpoints, etc.)
```

### `environments/` - Environment Configs

```text
environments/
└── environment.ts             # Environment-specific config file (ignore this file before pushing)
```
---

## How to Use This Structure

- **Add new features**: Create a new folder under `pages/` for each feature or page.
- **Shared components**: Place reusable components in `shared/`.
- **Core services/utilities**: Add singleton services, guards, interceptors, and models in `core/`.
- **Assets and styles**: Organize images, fonts, and styles in the `assets/` directory.
- **Layouts**: Place header, footer, and other layout components in `layouts/`.

### Example Workflow

1. **Generate a new component**:
   ```bash
   ng generate component pages/feature-name/feature-component
   ```
2. **Add a service**:
   ```bash
   ng generate service core/services/feature
   ```
3. **Add global styles**: Edit or add SCSS files in `assets/scss/`.

---

This structure encourages separation of concerns, reusability, and maintainability for Angular projects.

- Each folder is organized by feature and responsibility for clarity and scalability.
- You can expand or add new folders as your project grows.
