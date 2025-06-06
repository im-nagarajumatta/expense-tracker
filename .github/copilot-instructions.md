# GitHub Copilot Custom Instructions for Expense Tracker

## <bootstrap-styling>
Use Bootstrap v5.3.x for all HTML templates.  
- Use responsive grid layout for form and table alignment  
- Use `form-control`, `form-group`, and `btn` classes for consistent form design  
- Display success or error feedback using Bootstrap `alert` components  
- Use `table` and `table-striped` for expense listing  
- Include `navbar` for site navigation and `card` for wrapping sections  
- Ensure modals and other JavaScript-powered components are initialized properly  
- Prioritize mobile responsiveness with appropriate breakpoints (`col-md-*`, `col-lg-*`)  
</bootstrap-styling>

## <css-styling>
Organize styling using SCSS:  
- Follow BEM (Block Element Modifier) naming convention  
- Structure styles by component (e.g., `_form.scss`, `_table.scss`, `_navbar.scss`)  
- Use CSS variables for color and spacing consistency  
- Include animations/transitions for form interactions and alerts  
- Add media queries for form layout and table responsiveness  
- Override Bootstrap styles cleanly within component SCSS files  
</css-styling>

## <api>
Use FastAPI to handle form submissions and data listing:  
- Use `@app.get("/")` to render the homepage with a list of expenses  
- Use `@app.post("/add")` to process submitted form data  
- Use Pydantic models to validate and structure expense input (`title`, `amount`, `category`, `date`)  
- Return proper status codes (`201 Created` for success, `400 Bad Request` on error)  
- Use async functions for database I/O  
- Ensure HTML form submits data as `application/x-www-form-urlencoded`  
- Use Jinja2 to render expenses from API response  
</api>

## <error-handling>
Ensure robust error handling in both API and frontend:  
- Wrap database operations in `try-except` blocks  
- Use FastAPI `HTTPException` with meaningful messages for client feedback  
- Register global exception handlers for 404, 422, and validation errors  
- Show error or success messages on the frontend using Bootstrap `alert-danger` or `alert-success`  
- Log exceptions using the `logging` module for backend debugging  
</error-handling>
