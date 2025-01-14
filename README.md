# Validation Application Demo

This project demonstrates form validation using Spring MVC and custom annotations.

## Features
- Validates user input using built-in and custom annotations.
- Displays error messages for invalid form entries.
- Confirms valid submissions with a summary page.

## Project Structure

### 1. Customer Class
Handles user details with the following validations:
- `firstName`: Optional field.
- `lastName`: Required (`@NotNull` and `@Size(min = 1)`).
- `freePasses`: Must be between 0 and 10 (`@Min(0)` and `@Max(10)`).
- `postalCode`: Must be 5 alphanumeric characters (`@Pattern`).
- `courseCode`: Must start with "TOPS" (custom `@CourseCode` annotation).

### 2. CourseCode Custom Annotation
- Ensures the `courseCode` starts with a specific prefix (default: "LUV").
- The `CourseCodeConstraintValidator` handles validation logic.

### 3. Frontend (Thymeleaf Templates)
- **customer-form.html**: Form for entering customer details with validation error messages.
- **customer-confirmation.html**: Displays the user's submitted information upon successful validation.

## How to Run
1. Clone the project.
2. Set up a Spring Boot environment.
3. Access the form at `/showForm`.
4. Submit the form to see validation in action.

## Dependencies
- Spring MVC
- Thymeleaf
- Jakarta Bean Validation (Jakarta EE)
- Bootstrap (for styling)
