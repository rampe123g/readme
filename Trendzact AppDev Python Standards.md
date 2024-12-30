# Trendzact R&D Project Best Practices, Conventions and Template 

# Product Lifecycle for Small App Development Team

## Ideation & Planning
-   **Activities**:
    -   Brainstorm product ideas and features.
    -   Define MVP (Minimum Viable Product) scope.
    -   Create a product backlog and prioritize user stories.
-   **Tools**:
	- **Figma** for UI design.
		- [Team Files Link](https://www.figma.com/files/team/1454156970045387994)
    -   **StackEdit**:  .md editor for documentation and team wikis.
	-  **Gherkin** format for test cases
	- **Mermaid** for .md charts and graphs - documentation
		 - https://www.mermaidchart.com/  
    -   **AWS CodeCatalyst**: Backlog creation and sprint planning.
-   **Deliverables**:
    -   Wireframes.
    -   Product roadmap.
    -   Sprint backlog.

## MVP Stage
 -   **Activities**:
    -   Identify essential features for the MVP and create user stories.
    -   Focus on rapid prototyping and testing.
    -   Deploy to a staging environment for feedback from early adopters.
 -   **Tools**:
 - 
	 - **GitHub** for code repo and version control
			 - Might change to AWS CodeCommit at a later date
	- **AI Code Tools**
		- AWS DevQ with AmazonQ for Jetbrains
		- Anthropic Claude
		- Jetbrains ChatGPT
		- GitHub CoPilot AI Codebot
	-  **PyCharm** (Python) and **WebStorm** (React).
	-  **pytest-bdd**
	-  Use  ***venv*** to isolate dependencies.
	```python
		-m venv venv
		venv\Scripts\activate
		deactivate
	```
 - *** Internationalization (i18n)***
	 - Use `react-i18next` for internationalization in React. Metronic works well with `react-i18next` because of its component-based architecture.
	 - See Stub Code Section

 - Use **apppaths.py** for managing application paths. This template is scalable and includes configurations for both local file paths and S3 integration. See stub file.
`npm install i18next react-i18next i18next-browser-languagedetector i18next-http-backend'


    -   **AWS CodeCatalyst**: Automate CI/CD pipelines and manage project tasks.
	    - 	Amazon CodeCatalyst is one place where you can plan work, collaborate on code, and build, test, and deploy applications with continuous integration/continuous delivery (CI/CD) tools
		 - https://codecatalyst.aws/spaces/typeacyclist_mattg/projects
		 - https://docs.aws.amazon.com/codecatalyst/
		 - https://docs.aws.amazon.com/codecatalyst/latest/userguide/getting-started-template-project.html
		 - https://aws.amazon.com/blogs/devops/quickly-go-from-idea-to-pr-with-codecatalyst-using-amazon-q/
    -   **AWS Amplify with React**: Backend and frontend development.
	    - [React Concepts](https://docs.amplify.aws/react/how-amplify-works/concepts/)
		  - [UI Components](https://ui.docs.amplify.aws/)
		 - https://docs.amplify.aws/react/how-amplify-works/concepts/
		 - https://docs.amplify.aws/react/
		 - https://ui.docs.amplify.aws/
    -   **Metronic Bootstrap**: Use for pre-built components, responsive design, and rapid UI development.
        -   [Metronic Bootstrap Documentation](https://keenthemes.com/metronic/bootstrap)
        - 	 https://keenthemes.com/metronic/docs
		 - https://keenthemes.com/metronic/bootstrap
		 - Bootstrap Options: [Details](https://keenthemes.com/metronic/bootstrap)
		    -   Deliver projects quickly with ready-made components.
			-   Prefers traditional, component-based workflows.
			-   Consistent, standard look is sufficient.

		***See Metronic Tailwind for demos only***
		https://keenthemes.com/metronic/tailwind/docs/
		https://keenthemes.com/metronic/tailwind/docs/getting-started/integration/react
		https://keenthemes.com/metronic/tailwind/react/demo1/auth/login
-   **Other Tools**:
	-   **Pandas Profiling**: For quick exploratory data analysis (EDA).
	-   **JupyterLab**: For data science workflows and visualizations.
	-   **Scikit-learn**: For lightweight machine learning if needed in the project.
-   **Hosting**:
    -   **AWS Free Tier**: Use services like EC2, Lambda, and Amplify to minimize initial costs.
	-  **Serverless**
-   **Deliverables**:
    -   MVP deployed to a staging or limited production environment.
    -   Feedback gathered from early adopters.
    -   Actionable insights for future iterations.

## Development
-   **Activities**:
    -   Implement features in sprints.
    -   Write and maintain unit, integration, and end-to-end tests.
    -   Set up CI/CD pipelines for continuous integration and deployment.
-   **Tools**:
    -   **JetBrains PyCharm** (Python) and **JetBrains WebStorm** (React).
    -   **AWS CodeCommit**: Version control.
    -   **Docker**: Containerization.
    -   **AWS CodeBuild** and **AWS CodePipeline**: CI/CD workflows.
	-   **Use React with AWS Amplify**:
		    -   If you prefer a serverless and managed solution with minimal backend setup.
		    -   Ideal for frontend-heavy projects where backend complexity is low.
	-   **Use Flask/Django**:
		    -   If your application has custom backend requirements or relies on a relational database.
	-   **Use Both**:
		    -   For scalable, modern full-stack applications needing both a strong backend and a dynamic frontend.
	-    **AWS Secrets Manager** migrate to Secrets sensitive data in CI/CD pipelines
	-    **AWS Cloudfront** is it needed for Amplify
	-    **Amazon API Gateway**: Test and validate APIs directly with integrated testing tools.
	-   **Amazon CloudWatch**: Monitor logs, metrics, and errors for the MVP in real time.
	-   **Amazon CloudWatch Synthetics**: Monitoring and testing web applications via canaries (automated scripts simulating user interactions). Lightweight and automated, ideal for ongoing monitoring and simple E2E testing.  [CloudWatch Synthetics](https://docs.aws.amazon.com/AmazonCloudWatch/latest/monitoring/CloudWatch_Synthetics.html)
	- **Automated Documentation Updates**:
	-   Use tools like ***Swagger/OpenAPI*** for backend APIs to ensure the documentation evolves with the codebase.
-   **Hosting**:
    -   **AWS Elastic Beanstalk**: Deploy backend services.
    -   **AWS Amplify**: Host and manage frontend React apps.
-   **Deliverables**:
    -   Features deployed to staging environment.
    -   Automated tests with >80% coverage.
    -   Updated sprint board.

## Testing & Quality Assurance
-   **Activities**:
    -   Execute manual and automated tests.
    -   Perform usability and performance testing.
    -   Resolve bugs and retest.
-   **Tools**:
	-   **Amazon API Gateway**: API testing with built-in mock integrations and testing tools.
	-   **Amazon CloudWatch**: Log and monitor application errors, performance, and metrics.
	-   **JetBrains Gateway**: Remote environment testing for seamless cloud-hosted debugging and development.
	-   **JetBrains Qodana**: Static analysis and code quality inspection.
    -   **BrowserStack**: Cross-browser testing.
-   **Deliverables**:
    -   Test reports.
    -   Stable release candidates.
    -   Updated documentation.

## Deployment
-   **Activities**:
    -   Deploy to production environment.
    -   Monitor post-deployment performance.
    -   Roll back if issues arise.
-   **Tools**:
    -   **AWS CodeDeploy**: Automates deployment to EC2 instances or Lambda.
    -   **AWS CloudFront**: CDN for frontend distribution.
    -   **AWS CDK CloudFormation**: Infrastructure as Code (IaC).
-   **Deliverables**:
    -   Live production environment.
    -   Deployment documentation.
    -   Rollback plans.

## Monitoring & Maintenance

-   **Activities**:
    -   Monitor application health and user feedback.
    -   Optimize performance and scalability.
    -   Schedule regular maintenance updates.
-   **Tools**:
	-   **Amazon CloudWatch**: Advanced performance monitoring and logging.
	    -   Track metrics, logs, and alarms for backend, frontend, and infrastructure performance.
	-   **AWS X-Ray**: Distributed tracing for identifying performance bottlenecks and debugging complex applications.
	-   **Amazon DevOps Guru**: Leverage machine learning to detect anomalies and provide insights into operational performance.
-   **Deliverables**:
    -   Monitoring dashboards.
    -   Issue resolution reports.
    -   Regular maintenance schedules.

## Process Controls

-   **Version Control**:
        -   Use **GitHub** for MVP then **AWS CodeCommit** for Development with **main** as the primary branch.
    -   Enforce branch protection rules for **main**:
        -   Require pull request reviews before merging.
        -   Automate testing and linting with GitHub Actions or AWS CodePipeline.
    -   Use **GitHub Collaborators** or AWS Identity and Access Management (**IAM**) for managing access.

-   **Code Style and Quality**:    
    -   **Python**:
        -   Follow `PEP 8` for Python code.
        -   Use `black` for auto-formatting.
        -   Use `flake8` for linting.
        -   Include a pre-commit hook to check formatting, linting, and security vulnerabilities (e.g., using `bandit`).
    -   **React**:
        -   Follow the **Airbnb React/JSX Style Guide**.
        -   Use `ESLint` and `Prettier` for linting and formatting.
        -   Add a pre-commit hook to enforce consistent formatting and ensure unit tests pass before committing.
-   **Code Reviews**:
        -   Use **GitHub Pull Requests** or **AWS CodeCatalyst Workflows**:
        -   Assign at least one reviewer for every PR.
        -   Require automated test results before merging.
-   **Environment and Configuration**:
        -   Use `.env` files for managing environment variables.
        -   Avoid committing `.env` files; add them to `.gitignore`.
        -   Use AWS Secrets Manager for securely managing sensitive information in production.

## File Structure

#### **Conventions**
-   **Python**:
    -   Use **snake_case** for filenames (e.g., `data_processor.py`).
    -   Keep relative file paths simple (e.g., `backend/app/a0_standard_file_01`).
    -   Keep filenames short but descriptive.
    -   Organize files into clear modules:
        -   Singular nouns for folders (`user/`, `product/`).
        -   Group helper functions in a dedicated utility folder (e.g., `utils/`).
        -   Use a `tests/` folder for unit tests and integration tests.
-   **React**:
    -   Use **PascalCase** for component filenames (e.g., `UserDashboard.jsx`).
    -   Organize files in a **feature-based structure**:
-   Use  relative file paths from **backend/app/a0_standard_file_01**
-   Files names are short
-   Functions should be descriptive
-   Singular nouns for folders (aX_module/, aX_template/, etc.)
-   Routes should be verbs (user_route.py)

## **Template Project Hybrid File Structure**
```plaintext
project_name/
├── backend/                      # Backend application (Python)
│   ├── app/                      # Main application package
│   │   ├── __init__.py           # Python Package initializer
│   │   ├── a0_standard_file_01   # Example workflow file
│   │   ├── z_app_paths.py        # Centralized app paths configuration
│   │   ├── z_config.py           # Global constants and parameters
│   │   ├── y_utils_app.py        # Application-specific helper functions
│   │   ├── z_utils_common.py     # Common helper functions
│   │   ├── z_main.py             # Entry point for the backend application
│   │   ├── assets_app/           # App-specific assets folder
│   │   │   ├── models/           # Machine learning or database models
│   │   │   ├── images/           # Images used by the app
│   │   │   ├── videos/           # Video files used by the app
│   │   ├── modules/              # Entity modules (e.g., user, product)
│   │   │   ├── __init__.py       # Module initializer
│   │   │   ├── a0_ie_user.py     # Example module for user-related logic
│   │   │   ├── b0_ie_product.py  # Example module for product-related logic
│   │   ├── api_routes/           # API/UI routes (controllers)
│   │   │   ├── __init__.py       # API initializer
│   │   │   ├── a0_routes.py      # Example API route definitions
│   │   ├── templates/            # HTML templates for server-side rendering
│   │   │   ├── ie_base.html      # Base template
│   │   │   ├── ie_user.html      # User-specific pages
│   │   │   ├── ie_product.html   # Product-specific pages
│   │   ├── static/               # Static assets served by the backend
│   │       ├── css/              # Stylesheets
│   │       ├── js/               # JavaScript files
│   │       ├── images/           # Static images
│   ├── database/                 # Database folder
│   │   ├── __init__.py           # Database initializer
│   │   ├── database_app.db       # SQLite database file
│   │   ├── schema.sql            # SQL schema
│   │   ├── z_utils_db/           # Utility functions for database interactions
│   ├── tests_backend/            # Backend test suite
│       ├── __init__.py           # Test initializer
│       ├── ie_test_routes.py     # Tests for API routes
│       ├── ie_test_models.py     # Tests for database models
│   ├── requirements.txt          # Backend Python dependencies
│   ├── Dockerfile                # Docker configuration for the backend
│   ├── README.md                 # Backend-specific readme
│   └── .env                      # Backend environment variables

├── frontend/                     # Frontend application (React)
│   ├── public/                   # Public files served directly
│   │   ├── index.html            # HTML entry point
│   │   ├── favicon.ico           # Favicon
│   ├── src/                      # React source code
│   │   ├── z_src_paths.js        # Centralized paths and constants
│   │   ├── components/           # Reusable React components
│   │   │   ├── Header.jsx        # Header component
│   │   │   ├── Footer.jsx        # Footer component
│   │   ├── pages/                # Page components
│   │   │   ├── Home.jsx          # Home page
│   │   │   ├── Products.jsx      # Products page
│   │   ├── services/             # API calls and client-side services
│   │   │   ├── api_services.js   # Handles API interactions
│   │   ├── assets/               # Static assets for React
│   │       ├── images/           # Images used in the frontend
│   │       ├── css/              # Stylesheets for the frontend
│   │       ├── fonts/            # Custom fonts
│   ├── package.json              # React dependencies and scripts
│   ├── Dockerfile                # Docker configuration for the frontend
│   ├── README.md                 # Frontend-specific readme
│   └── .env                      # Frontend environment variables

├── docs/                         # Project documentation
│   ├── installation_guide.md     # Setup and installation instructions
│   ├── api_reference.md          # API reference documentation
│   ├── architecture.md           # Application architecture details
│   ├── database_design.md        # Database schema and relationships
│   ├── developer_guide.md        # Developer-specific guidelines
│   ├── troubleshooting.md        # Common issues and solutions
│   ├── changelog.md              # Record of changes in the project
│   └── api_flowchart.mermaid     # API flowchart (Mermaid.js format)

├── logs/                         # Logs directory
│   ├── frontend_logs/            # Logs specific to the frontend
│   ├── backend_logs/             # Logs specific to the backend

├── docker-compose.yml            # Docker Compose configuration for full-stack setup
├── .gitignore                    # Files to exclude from version control
├── README.md                     # Main high-level project overview
└── .env                          # Global environment variables
```

### **Hybrid File Structure Key Considerations**
1.  **Shared Environment**:    
    -   Use a **single `.env` file** at the project root for shared variables, like API endpoints and database URLs, but ensure sensitive data is managed securely using **AWS Secrets Manager** or **dotenv-safe**.
2.  **Docker Integration**:
        -   Use **Docker Compose** to run both the backend and frontend together during development and testing.
3.  **Testing**:
        -   Separate **tests_backend/** and **tests_frontend/** directories for clarity.
    -   Use a single CI/CD pipeline (GitHub Actions or AWS CodePipeline) to run tests for both.
4.  **Deployment**:
    
    -   Deploy the **frontend** using **AWS Amplify**.
    -   Deploy the **backend** using **AWS Elastic Beanstalk**, **ECS**, or **Lambda**.


## Standard Files

###  requirements.txt
    ```plaintext
    Flask==2.3.3
    Django==4.2
    requests==2.31.0
    SQLAlchemy==2.1.0
    pytest==7.4.2
    pytest-bdd==7.1.0
    black==23.9.1
    flake8==6.1.0
    python-dotenv==1.0.0
    ```
### .gitignore
```plaintext
# Byte-compiled / optimized / DLL files
__pycache__/
*.py[cod]
*$py.class

# C extensions
*.so

# Virtual environment
env/
venv/
ENV/
.venv/
env.bak/
env.d/

# Django stuff:
*.log
local_settings.py

# Flask stuff:
instance/
.webassets-cache

# Python test discovery
.pytest_cache/
.tox/
.cache/
.coverage
coverage.xml
nosetests.xml
*.cover
*.py,cover
.hypothesis/

# MyPy type-checking
.mypy_cache/

# Node.js
node_modules/
npm-debug.log*
yarn-debug.log*
yarn-error.log*

# React build files
build/

# AWS environment files
*.env
.env.local
.env.development.local
.env.test.local
.env.production.local

# Logs and databases
*.log
*.sqlite3

# Editor directories and files
.idea/
.vscode/
*.swp
*.swo
.DS_Store

# Docker files
*.log
docker-compose.override.yml

# AWS SAM
.aws-sam/
```

### app_paths.py
    ```python
    import os
    
    BASE_DIR = os.path.dirname(os.path.abspath(__file__))
    
    # Paths for assets
    STATIC_DIR = os.path.join(BASE_DIR, 'static')
    TEMPLATES_DIR = os.path.join(BASE_DIR, 'templates')
    IMAGES_DIR = os.path.join(STATIC_DIR, 'images')
    CSS_DIR = os.path.join(STATIC_DIR, 'css')
    
    # Database path
    DATABASE_PATH = os.path.join(BASE_DIR, 'database', 'database_app.db')
    
    ```
### Behavior-Driven Design Tests (Gherkin)
**Best Practice**: Store Gherkin files under `tests/feature/`.
```gherkin
Feature: User Login
  As a user
  I want to log in to the application
  So that I can access my dashboard

  Scenario: Successful Login
    Given I am on the login page
    When I enter valid credentials
    Then I should be redirected to my dashboard

  Scenario: Unsuccessful Login
    Given I am on the login page
    When I enter invalid credentials
    Then I should see an error message

from pytest_bdd import scenario, given, when, then
# Scenario linking
@scenario('features/login.feature', 'Successful Login')
def test_successful_login():
    pass

@scenario('features/login.feature', 'Unsuccessful Login')
def test_unsuccessful_login():
    pass

# Step definitions
@given('I am on the login page')
def login_page():
    # Setup for the login page
    print("Navigating to the login page.")

@when('I enter valid credentials')
def enter_valid_credentials():
    # Simulate entering valid credentials
    print("Entering valid credentials.")

@when('I enter invalid credentials')
def enter_invalid_credentials():
    # Simulate entering invalid credentials
    print("Entering invalid credentials.")

@then('I should be redirected to my dashboard')
def redirected_to_dashboard():
    # Assert the user is redirected to the dashboard
    print("Redirected to the dashboard.")
    assert True

@then('I should see an error message')
def see_error_message():
    # Assert an error message is displayed
    print("Error message displayed.")
    assert True
```

## Logging
**Best Practice**: Use `CloudWatch Logs` for production deployments on AWS.
**Usage Tips for MVP Teams**
pip install loguru
-   Use **DEBUG** during development to log detailed information.
-   Switch to **INFO** or **WARNING** in production to avoid cluttered logs.
-   Combine **Loguru** with **AWS CloudWatch Logs** for centralized monitoring in production environments:
    -   Add a handler to send logs to CloudWatch.
-   Structure your application to log exceptions using Loguru’s built-in decorators:
```python
    `@logger.catch
    def faulty_function():
        return 1 / 0  # This will log the exception automatically`
```

```python
	from loguru import logger
	import os

	# Configure the log file location
	LOG_DIR = os.path.join(os.path.dirname(__file__), "logs")
	os.makedirs(LOG_DIR, exist_ok=True)  # Ensure the logs directory exists

	LOG_FILE = os.path.join(LOG_DIR, "app.log")
	
	# Loguru Configuration
	logger.add(
    LOG_FILE,
    format="{time:YYYY-MM-DD HH:mm:ss} | {level} | {message}",
    level="INFO",  # Adjust the logging level as needed (e.g., DEBUG, INFO, WARNING, ERROR)
    rotation="1 MB",  # Automatically rotate log files when they exceed 1 MB
    retention="7 days",  # Keep logs for 7 days before deletion
    compression="zip",  # Compress rotated log files
	)

	# Example Usage
	if __name__ == "__main__":
    logger.debug("This is a debug message.")
    logger.info("Application started successfully.")
    logger.warning("This is a warning.")
    logger.error("An error occurred!")
    logger.critical("Critical issue detected!")
   ```

## Pre-Commit Hook**

-   **Purpose**: Automate checks before committing code.
-   **Template** (`.pre-commit-config.yaml`):
    
    ```yaml
    repos:
      - repo: https://github.com/pre-commit/pre-commit-hooks
        rev: v4.5.0
        hooks:
          - id: check-yaml
          - id: end-of-file-fixer
          - id: trailing-whitespace
    
      - repo: https://github.com/psf/black
        rev: 23.9.1
        hooks:
          - id: black
    
      - repo: https://github.com/pycqa/flake8
        rev: 6.1.0
        hooks:
          - id: flake8
    
    ```
    

----------

### **6. README Template**

-   **Purpose**: Provide high-level project information.
    
-   **Template**:
    
    ```markdown
    # Project Name
    
    ## Description
    Briefly describe the project.
    
    ## Installation
    ```bash
    pip install -r requirements.txt
    npm install
    
    ```
    
    ## Usage
    
    ```bash
    python backend/app/z_main.py
    npm start
    
    ```
    
    ## Testing
    
    Run backend and frontend tests:
    
    ```bash
    pytest
    npm test
    
    ```
    

----------

### **7. `pytest` with `pytest-bdd`**

-   **Purpose**: Automate tests for behavior-driven development.
-   **Template**:
    
    ```python
    from pytest_bdd import scenarios, given, when, then
    
    # Link to feature file
    scenarios('features/login.feature')
    
    @given('I am on the login page')
    def login_page():
        # Setup for login page
        pass
    
    @when('I enter valid credentials')
    def enter_credentials():
        # Code to simulate entering credentials
        pass
    
    @then('I should be redirected to my dashboard')
    def verify_dashboard():
        # Assert dashboard presence
        assert True
    
    ```
    

----------

### **8. Docker Compose**

-   **Purpose**: Orchestrate services for the project.
-   **Template**:
    
    ```yaml
    version: '3.8'
    
    services:
      backend:
        build: ./backend
        ports:
          - "5000:5000"
        environment:
          - FLASK_ENV=development
        volumes:
          - ./backend:/app
    
      frontend:
        build: ./frontend
        ports:
          - "3000:3000"
        volumes:
          - ./frontend:/app
    
    ```
    

----------

### **9. `.env`**

-   **Purpose**: Manage environment variables.
-   **Template**:
    
    ```plaintext
    FLASK_ENV=development
    DATABASE_URL=sqlite:///database/database_app.db
    AWS_ACCESS_KEY_ID=your_key_id
    AWS_SECRET_ACCESS_KEY=your_secret_key
    
    ```
    
### apppaths.py code
```python
	from pathlib import Path
	import os

	class AppPaths:
	    """
	    A centralized class for managing application paths, both local and remote (S3).
	    """
	    
	    # Get the root directory of the project
	    ROOT_DIR = Path(__file__).parent.parent.absolute()
	    
	    # Application directories
	    APP_DIR = ROOT_DIR / 'app'
	    ASSETS_DIR = APP_DIR / 'assets'
	    TEMPLATES_DIR = APP_DIR / 'templates'
	    STATIC_DIR = APP_DIR / 'static'

	    # Log and Database directories
	    LOGS_DIR = ROOT_DIR / 'logs'
	    DATABASE_DIR = ROOT_DIR / 'database'
	    DATABASE_FILE = DATABASE_DIR / 'app.db'

	    # S3 Configuration (loaded from environment variables)
	    S3_BUCKET = os.getenv('S3_BUCKET', 'default-bucket-name')  # Replace 'default-bucket-name' as needed
	    S3_PREFIX = os.getenv('S3_PREFIX', 'my-app')

	    @staticmethod
	    def get_s3_path(relative_path: str) -> str:
	        """
	        Convert a local relative path to an S3 path.
	        
	        Args:
	            relative_path (str): The relative path to convert.
	        
	        Returns:
	            str: The full S3 path.
	        """
	        if not AppPaths.S3_BUCKET:
	            raise ValueError("S3_BUCKET environment variable is not set.")
	        return f"s3://{AppPaths.S3_BUCKET}/{AppPaths.S3_PREFIX}/{relative_path}"

	    @staticmethod
	    def get_local_path(relative_path: str) -> Path:
	        """
	        Get the absolute local path for a given relative path.
	        
	        Args:
	            relative_path (str): The relative path to convert.
	        
	        Returns:
	            Path: The absolute local path.
	        """
	        return AppPaths.ROOT_DIR / relative_path

	    @staticmethod
	    def ensure_directories():
	        """
	        Ensure all critical directories exist.
	        """
	        directories = [
	            AppPaths.APP_DIR,
	            AppPaths.ASSETS_DIR,
	            AppPaths.LOGS_DIR,
	            AppPaths.DATABASE_DIR,
	            AppPaths.STATIC_DIR,
	        ]
	        for directory in directories:
	            directory.mkdir(parents=True, exist_ok=True)

	# Example usage
	if __name__ == "__main__":
	    print(f"Root Directory: {AppPaths.ROOT_DIR}")
	    print(f"Logs Directory: {AppPaths.LOGS_DIR}")
	    print(f"Database File: {AppPaths.DATABASE_FILE}")
	    print(f"S3 Path for 'test.txt': {AppPaths.get_s3_path('test.txt')}")
	    print(f"Local Path for 'config.yaml': {AppPaths.get_local_path('config.yaml')}")
	    AppPaths.ensure_directories()
```

### **How to Use apppaths.py**

**Set Environment Variables**:
    
    -   Define `S3_BUCKET` and `S3_PREFIX` in your `.env` file or environment.
        
        plaintext
        
        Copy code
        
        `S3_BUCKET=my-app-bucket
        S3_PREFIX=my-app-prefix` 
        
**Access Paths**:
    
    -   Use `AppPaths.LOGS_DIR` for the logs directory or `AppPaths.get_s3_path('file.txt')` for S3 paths.
**Integrate with the Application**:
    
    -   Use `AppPaths.ensure_directories()` at the application startup to ensure all required directories exist.




----------

### **Internationalization with React and Metronic**
If you're using **React** and **Metronic**, integrating internationalization (i18n) with support for Simplified Chinese (zh-CN) and Traditional Chinese (zh-TW) can be streamlined using the following approach:

#### **1. Install Dependencies**

Use `react-i18next` for internationalization in React. Metronic works well with `react-i18next` because of its component-based architecture.

bash

Copy code

`npm install i18next react-i18next i18next-browser-languagedetector i18next-http-backend` 

#### **2. Prepare Translation Files**

Create JSON translation files for each language in the `public/locales` directory.

plaintext

Copy code

`public/locales/
├── zh_CN/
│   ├── translation.json
├── zh_TW/
│   ├── translation.json
├── en/
    ├── translation.json` 

Example `translation.json`:

-   **Simplified Chinese (zh_CN/translation.json)**:
    
    json
    
    Copy code
    
    `{
      "welcome": "欢迎使用我们的应用程序！",
      "login": "登录",
      "logout": "登出"
    }` 
    
-   **Traditional Chinese (zh_TW/translation.json)**:
    
    json
    
    Copy code
    
    `{
      "welcome": "歡迎使用我們的應用程式！",
      "login": "登入",
      "logout": "登出"
    }` 
    
-   **English (en/translation.json)**:
    
    json
    
    Copy code
    
    `{
      "welcome": "Welcome to our application!",
      "login": "Login",
      "logout": "Logout"
    }` 
    

----------

#### **3. Initialize i18next**

Create an `i18n.js` file in your `src` folder to configure the i18n setup.

javascript

Copy code

`import i18n from 'i18next';
import { initReactI18next } from 'react-i18next';
import LanguageDetector from 'i18next-browser-languagedetector';
import HttpApi from 'i18next-http-backend';

i18n
  .use(HttpApi)
  .use(LanguageDetector)
  .use(initReactI18next)
  .init({
    supportedLngs: ['en', 'zh_CN', 'zh_TW'],
    fallbackLng: 'en',
    detection: {
      order: ['path', 'cookie', 'htmlTag', 'localStorage', 'subdomain'],
      caches: ['cookie'],
    },
    backend: {
      loadPath: '/locales/{{lng}}/translation.json',
    },
  });

export default i18n;` 

----------

#### **4. Integrate with Metronic Components**

Replace hardcoded strings in Metronic's components with translation keys using `useTranslation` from `react-i18next`.

javascript

Copy code

`import React from 'react';
import { useTranslation } from 'react-i18next';

const Dashboard = () => {
  const { t } = useTranslation();

  return (
    <div>
      <h1>{t('welcome')}</h1>
      <button>{t('login')}</button>
      <button>{t('logout')}</button>
    </div>
  );
};

export default Dashboard;` 

----------

#### **5. Add Language Switcher**

Create a language switcher dropdown using Metronic's styling.

javascript

Copy code

`import React from 'react';
import i18n from 'i18next';
import { Dropdown } from 'react-bootstrap';

const LanguageSwitcher = () => {
  const changeLanguage = (lang) => {
    i18n.changeLanguage(lang);
  };

  return (
    <Dropdown>
      <Dropdown.Toggle variant="success" id="dropdown-basic">
        Language
      </Dropdown.Toggle>

      <Dropdown.Menu>
        <Dropdown.Item onClick={() => changeLanguage('en')}>English</Dropdown.Item>
        <Dropdown.Item onClick={() => changeLanguage('zh_CN')}>简体中文</Dropdown.Item>
        <Dropdown.Item onClick={() => changeLanguage('zh_TW')}>繁體中文</Dropdown.Item>
      </Dropdown.Menu>
    </Dropdown>
  );
};

export default LanguageSwitcher;` 

----------

#### **6. Integrate into Layout**

Add the language switcher to Metronic's header or footer to allow users to select their preferred language.

In the Metronic `src/_metronic/layout/components/header/Header.tsx` (or similar), integrate the `LanguageSwitcher`:

javascript

Copy code

`import LanguageSwitcher from './LanguageSwitcher';

const Header = () => {
  return (
    <div className="header d-flex align-items-center justify-content-between">
      <h2>My App</h2>
      <LanguageSwitcher />
    </div>
  );
};

export default Header;` 

----------

### **7. Dynamic Language Detection**

To detect the user’s preferred language dynamically, enable browser-based detection in `i18n.js`. This will automatically pick the user's browser settings and apply the appropriate language.

----------

### **8. Test Translation Integration**

-   **Language Switching**: Verify that switching languages updates all components dynamically.
-   **Default Language**: Ensure the app defaults to English (or any fallback language) if translations are missing.
-   **UI Consistency**: Ensure Metronic's components render correctly for all languages, especially for text-heavy sections.

----------

### **9. Lazy Load Translations**

Optimize performance by lazy-loading translation files. This is already supported in `i18next` through `i18next-http-backend`.

----------

### **10. Deployment Considerations**

-   **CDN for Translation Files**: Host `public/locales` on a CDN like AWS CloudFront for fast global access.
-   **Cache Headers**: Set appropriate cache headers to reduce load times for frequently accessed locales.

----------

With this implementation, your React application built on Metronic can support Simplified and Traditional Chinese seamlessly while maintaining a scalable and modular architecture. Let me know if you'd like code examples for specific Metronic components!
