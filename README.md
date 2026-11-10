# DataCanvas: Client-Side Exploratory Data Analysis Studio
### COMP3421 Web Application Design and Development — Final Project
**Author:** Chan Kwing Hei (Student ID: 25128829D)  
**Course Route:** AI Vibe coding route
**Deployment Link:** [https://github.io](https://github.io) (Example)

---

## 📋 Project Overview
**DataCanvas** is a lightweight, zero-dependency, 100% client-side Exploratory Data Analysis (EDA) and visualization dashboard. It solves a modern web privacy issue: analyzing sensitive CSV/JSON datasets without uploading data to third-party cloud servers. 

By leveraging the **HTML5 File API**, **Blob API**, and native **HTML5 Canvas API**, all parsing, statistical evaluation, data mutations, and chart renders occur instantaneously within the user's browser sandbox.

### 🌟 Key Functional Features
*   **Secure Client-Side File Ingestion:** Drag-and-drop parsing for `.csv` and `.json` formats using non-blocking asynchronous file reader promises.
*   **Automated Data Profiling:** Instant inference of variable data types (Numeric vs. Categorical), alongside global metrics (Missing cells, rows, columns count).
*   **Univariate Descriptive Statistics:** Automated calculation of complex statistical parameters (Mean, Median, Standard Deviation, Q1, Q3, IQR) computed via optimized JavaScript math arrays.
*   **Interactive Graphics Sandbox:** Pure Canvas-driven visualization engine producing fully exportable frequency Bar charts, Line trends, and bivariate Scatter plots.
*   **Data Transformation & Export Engine:** Live relational database filtering simulator (`>`, `<`, `==`) executing downstream data mutations with dynamic local Blob downloading.

---

## 🛠️ Technology Stack & Architecture
*   **Client Interface:** Semantic HTML5, CSS3 Custom Properties (Variables), Flexbox, and CSS Grid for fluid element responsiveness down to 360px.
*   **Application Logic & Math Engine:** Vanilla ECMAScript 6+ structured using an object-oriented class architecture to maintain clean system states.
*   **Graphics Generation:** Native HTML5 Canvas API (Context 2D) rendering data points directly to pixels without heavy external charting library overhead.
*   **Storage & Persistence:** HTML5 Local File handles and transient object URLs generated dynamically via the browser's native `Blob` engine.

---

## 🚀 Installation & Local Reproducibility Guide
As a pure client-side application, **no server setup, database configuration, or `npm install` packages are required**. It runs natively out of the box.

### Prerequisites
*   A modern evergreen web browser (Google Chrome 110+, Mozilla Firefox 110+, Safari 16+, or Microsoft Edge).

### Steps to Run Locally
1.  **Clone or Download the Repository:** Extract the compressed archive containing `index.html`, `style.css`, and `app.js` into a unified directory.
2.  **Launch the Application:** 
    *   Double-click `index.html` to execute the code straight from your local system cache (`file:///` protocol), OR
    *   Run a lightweight development environment loop via Visual Studio Code's *Live Server* extension.
3.  **Load Test Account/Data:**
    *   Click the **⚡ Load Iris Dataset** quick-demo action button on the welcome banner to instantly feed mock variables into the system pipeline.

---

## 🧪 Testing Manifest Matrix

| Test Case ID | Target Feature | Vector / Action | Expected System Reaction | Result |
| :--- | :--- | :--- | :--- | :--- |
| TC-001 | Initialization | Launch application | Dashboard renders in `dashboard-empty` state with explicit "No dataset parsed yet" placeholder panel. | Pass |
| TC-002 | Format Guard | Drop a `.png` file | Intercepts action inside file handlers, blocks parsing loops, and displays an explicit format notification popup. | Pass |
| TC-003 | Math Profiling | Ingest Iris Demo CSV | Populates table rows automatically; calculates precise median, standard deviations, and quartile variables instantly. | Pass |
| TC-004 | Canvas Logic | Switch to Scatter | Clears older frames instantly; maps data array rows accurately to canvas pixel coordinate vectors with axis scales. | Pass |
| TC-005 | Filter Mutation | Apply condition (`< 3.0`) | Re-evaluates array collections instantly; updates metrics rows and table cells; renders custom chart distributions. | Pass |
