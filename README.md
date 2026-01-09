# React Forms

A modern, professional signup form built with React 19 and Vite. This project demonstrates form validation, state management using React's `useActionState` hook, and best practices for building accessible and user-friendly forms.

## Table of Contents

- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Technologies](#technologies)
- [Form Validation](#form-validation)
- [Available Scripts](#available-scripts)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

## Features

- ✅ **Modern React 19** - Built with the latest React features including `useActionState` hook
- ✅ **Form Validation** - Comprehensive client-side validation with custom validation utilities
- ✅ **User-Friendly UI** - Clean and intuitive signup form interface
- ✅ **Error Handling** - Detailed error messages displayed to users
- ✅ **Form State Persistence** - Form values are preserved on validation errors
- ✅ **Accessible** - Proper HTML semantics and labels for screen readers
- ✅ **Fast Development** - Powered by Vite for lightning-fast hot module replacement

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16 or higher)
- **npm** (v7 or higher) or **yarn**

You can check your versions by running:

```bash
node --version
npm --version
```

## Installation

1. Clone the repository:

```bash
git clone <your-repo-url>
cd react-forms
```

2. Install dependencies:

```bash
npm install
```

3. Start the development server:

```bash
npm run dev
```

4. Open your browser and navigate to the URL shown in the terminal (typically `http://localhost:5173`)

## Usage

### Signup Form

The signup form collects the following information:

- **Email** - Valid email address format required
- **Password** - Minimum 6 characters required
- **Confirm Password** - Must match the password field
- **First Name** - Required field
- **Last Name** - Required field
- **Role** - Selection from predefined options (Student, Teacher, Employee, Founder, Other)
- **Acquisition Channel** - How the user found us (checkboxes: Google, Referred by friend, Other)
- **Terms and Conditions** - Required agreement checkbox

### Form Submission

1. Fill in all required fields
2. Click the "Sign up" button
3. If validation fails, error messages will be displayed at the bottom of the form
4. Form values are preserved on validation errors for better user experience
5. Use the "Reset" button to clear all form fields

## Project Structure

```
react-forms/
├── public/
│   └── vite.svg
├── src/
│   ├── assets/
│   │   └── logo.jpg
│   ├── components/
│   │   ├── Header.jsx          # Header component with logo and title
│   │   └── Signup.jsx          # Main signup form component
│   ├── util/
│   │   └── validation.js       # Validation utility functions
│   ├── App.jsx                 # Main application component
│   ├── main.jsx                # Application entry point
│   └── index.css               # Global styles
├── index.html                  # HTML template
├── package.json                # Project dependencies and scripts
├── vite.config.js              # Vite configuration
└── README.md                   # Project documentation
```

## Technologies

- **React 19.0.0** - Latest React with modern hooks
- **Vite 5.2.0** - Next-generation frontend build tool
- **ESLint** - Code linting and quality assurance
- **JavaScript (JSX)** - Modern JavaScript with JSX syntax

## Form Validation

The form uses custom validation utilities located in `src/util/validation.js`:

### Validation Functions

- **`isEmail(value)`** - Checks if the value contains an '@' symbol (basic email validation)
- **`isNotEmpty(value)`** - Checks if the value is not empty after trimming whitespace
- **`hasMinLength(value, minLength)`** - Validates that the value meets the minimum length requirement
- **`isEqualToOtherValue(value, otherValue)`** - Compares two values for equality (used for password confirmation)

### Validation Rules

| Field | Validation Rules |
|-------|-----------------|
| Email | Must be a valid email format |
| Password | Required, minimum 6 characters |
| Confirm Password | Must match the password field |
| First Name | Required, cannot be empty |
| Last Name | Required, cannot be empty |
| Role | Required selection |
| Acquisition Channel | At least one option must be selected |
| Terms and Conditions | Must be checked |

## Available Scripts

In the project directory, you can run:

### `npm run dev`

Starts the development server with hot module replacement. The application will automatically reload when you make changes to the code.

### `npm run build`

Creates an optimized production build of the application in the `dist` folder. This build is ready for deployment.

### `npm run preview`

Preview the production build locally. Make sure to run `npm run build` first.

### `npm run lint`

Runs ESLint to check for code quality issues and potential bugs. The project is configured with React-specific linting rules.

## Development

### Code Style

This project uses ESLint with React-specific rules. Make sure your code follows the project's linting standards:

```bash
npm run lint
```

### Hot Module Replacement

Vite provides instant hot module replacement (HMR). Changes to your React components will be reflected immediately in the browser without a full page reload.

### Browser Support

This project targets modern browsers that support ES6+ features. For production use, consider adding polyfills if you need to support older browsers.

## Contributing

Contributions are welcome! If you'd like to contribute to this project:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please ensure your code follows the existing code style and passes all linting checks.

## License

This project is private and not licensed for public use.

---

Built with ❤️ using React and Vite
