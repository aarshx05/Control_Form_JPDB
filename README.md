# Control_Form_JPDB

# Employee Management Form

This project is a web-based employee management form that allows users to perform CRUD (Create, Read, Update, Delete) operations using the [JPDB API](https://login2explore.com/jpdb/docs.html) and JavaScript. The form enables users to add new employees, edit existing employee details, navigate between records, and reset the form. It is designed to provide a seamless experience for managing employee data.

## Features

- **Add New Employee**: Easily add a new employee's details.
- **Edit Employee Data**: Update employee information.
- **Save Employee Information**: Save changes to employee records.
- **Form Reset**: Clear the form to its initial state.
- **Navigation**: Navigate through employee records with buttons for first, previous, next, and last records.
- **Validation**: Ensures that all required fields are filled before saving or updating a record.

## Prerequisites

- **Knowledge of HTML, JavaScript, and jQuery** is needed to work on the project.
- **JPDB Account**: You need a JPDB account and a connection token to use the JPDB API.
- **Server Setup**: The JPDB server URL must be configured correctly.

## Technologies Used

- **HTML** for structuring the form.
- **JavaScript & jQuery** for client-side scripting.
- **JPDB API** for backend integration.
- **CSS (optional)** for basic styling (can be extended for better design).

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/employee-management-form.git
   ```

2. **Set Up JPDB Connection**
   - Create a JPDB account if you haven't already.
   - Set up a database and relation for employee data in JPDB.
   - Obtain the connection token and update the `connToken` variable in the code.

3. **Configure the Database and Relation**
   - Update the variables in the script to match your JPDB configuration:
     ```javascript
     const connToken = "YOUR_CONNECTION_TOKEN";
     const baseURL = "http://api.login2explore.com:5577";
     const empDBName = "Emp-DB"; // Change to your database name
     const empRelationName = "EmpData"; // Change to your relation name
     ```

4. **Open `index.html` in a web browser**
   - You can directly open the `index.html` file in your browser or host it on a local server (e.g., using [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) in VS Code).

## Project Structure

```
employee-management-form/
├── index.html            # The main HTML file for the form
├── script.js             # JavaScript file with all the form logic
└── style.css             # Optional CSS file for styling the form
```

## Functionalities

1. **Initialization (`initEmpForm`)**
   - Initializes the form state on page load.
   - Disables all form fields and controls, except for the `New` button.
   
2. **Adding New Records (`newData`)**
   - Clears the form fields.
   - Enables input for adding a new employee record.

3. **Saving Records (`saveData`)**
   - Saves the new employee data or changes to the existing record.

4. **Editing Existing Records (`editData`)**
   - Enables form fields for updating an existing employee's details.
   
5. **Changing Data (`changeData`)**
   - Saves changes made to an existing employee's details.

6. **Navigating Records (`getFirst`, `getPrev`, `getNext`, `getLast`)**
   - Allows navigation through the records with dedicated buttons.
   - Disables buttons where appropriate, e.g., when at the first or last record.

7. **Resetting the Form (`resetForm`)**
   - Reverts the form to its initial state.

## Form Validation

The form ensures that all fields are filled out before allowing the user to save or update data. The fields include:

- Employee ID
- Employee Name
- Basic Salary
- HRA (House Rent Allowance)
- DA (Dearness Allowance)
- Deductions

## Screenshots




## Future Enhancements

- Implement better styling for a more user-friendly interface.
- Add pagination for handling large data sets.
- Integrate search functionality to quickly find employee records.
- Implement user authentication to secure the form.

## Contributing

Contributions are welcome! If you have suggestions or improvements, please create a pull request or open an issue.

## License

This project is open-source and available under the MIT License.
