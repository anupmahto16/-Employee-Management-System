### Employee Management System

This project involves creating an Employee Management System that allows users to manage and view employee data interactively. The system utilizes a remote API to fetch, filter, sort, and paginate employee data displayed on a web interface.

#### Features

- **Dynamic Data Fetching:** Fetch employee data from the remote API.
- **Table Display:** Display employee data in a table format with columns for Serial Number, Name, Gender, Department, and Salary.
- **Filtering Options:**
  - **By Department:** Dropdown to select and filter employees by their department.
  - **By Gender:** Dropdown to select and filter employees by their gender.
- **Sorting Option:**
  - **By Salary:** Dropdown to sort employees based on their salary in ascending or descending order.
- **Pagination Controls:** Buttons to navigate through pages of data with functionality to handle edge cases (e.g., disable the previous button on the first page and the next button on the last page).

#### Implementation Details

1. **API Usage:** The base URL for the API is `https://dbioz2ek0e.execute-api.ap-south-1.amazonaws.com/mockapi/get-employees`. This API supports several query parameters:
   - `page`: Specifies the current page of data.
   - `limit`: Specifies the number of records per page.
   - `filterBy`: Specifies the field used for filtering (either `department` or `gender`).
   - `filterValue`: Specifies the value for the filter.
   - `sort`: Specifies the field used for sorting.
   - `order`: Specifies the sorting order (`asc` or `desc`).

2. **Pagination Implementation:** Pagination is handled dynamically based on the total number of records and the selected `limit`. The frontend will adjust the available pages as the filters or sorts change.

3. **Dropdown Controls:** Each dropdown control modifies the API query parameters to fetch the filtered or sorted data accordingly.

4. **Data Rendering:** Data fetched from the API is rendered in an HTML table. The table updates based on the applied filters, sort, and pagination.

#### Usage Instructions

1. **Setup:**
   - Clone the repository and navigate into the project directory.
   - Install dependencies if necessary (e.g., if using a JavaScript framework).
   - Open the index.html file in a web browser to start using the application.

2. **Interacting with the System:**
   - Use the "Select Department" dropdown to filter employees by department.
   - Use the "Select Gender" dropdown to filter employees by gender.
   - Use the "Select Order" dropdown to sort employees by salary.
   - Use the pagination buttons at the bottom of the page to navigate between pages.
   - Filters and sorting preferences are preserved across pagination.

3. **Limitations and Assumptions:**
   - Assumes stable internet connectivity for API calls.
   - Assumes the API handles errors gracefully and returns appropriate messages.

#### Technologies Used

- HTML/CSS for the frontend layout and styling.
- JavaScript for dynamic interaction with the API and DOM manipulation.
- Optional: A JavaScript framework like React or Vue for more complex state management and component-based architecture.

