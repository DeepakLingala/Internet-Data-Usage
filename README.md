# Data Usage Analyzer

A Python-based GUI application for analyzing and visualizing internet data usage. This project combines the functionality of user login and registration with the ability to analyze internet data usage through bar graphs and pie charts. Built using **Tkinter** for the GUI, **MySQL** for authentication, and **Pandas** for data processing.

---

## Features

### User Authentication
- **Login**: Users can log in to access the application's main features.
- **Register**: New users can register and store their credentials securely in a MySQL database.

### Data Visualization
- **Bar Graph**: Visualizes the top 10 applications with the highest data usage.
- **Pie Chart**: Displays the percentage distribution of data usage across applications.
- **Data Display**: Presents the raw data in a tabular format.

### Data Processing
- Parses data usage from a CSV file (`Internet-Data-Usage.csv`).
- Handles data in multiple formats (e.g., KB, MB, GB) and converts it into MB for consistent analysis.

---

## Prerequisites

### Python Libraries
Ensure the following Python libraries are installed:
- `tkinter` (Built-in with Python)
- `mysql-connector-python`
- `pandas`
- `matplotlib`

You can install the required libraries using pip:
```bash
pip install mysql-connector-python pandas matplotlib
```

### Database Setup
1. Set up a MySQL database named `internet-data-usage`.
2. Create a table for user credentials:
```sql
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) UNIQUE NOT NULL,
    password VARCHAR(255) NOT NULL
);
```

### Data File
Ensure the file `Internet-Data-Usage.csv` is present in the same directory as the script. The file should have the following structure:

| LIST OF APPILICATIONS | DATA USAGE PER APPILICATION |
|-----------------------|----------------------------|
| Application1          | 10 MB                     |
| Application2          | 50 KB                     |
| Application3          | 1 GB                      |

---

## How to Use

1. **Clone the Repository**:
   ```bash
   git clone <repository-url>
   cd data-usage-analyzer
   ```

2. **Run the Application**:
   Execute the Python script:
   ```bash
   python data_usage_analyzer.py
   ```

3. **Login or Register**:
   - New users must register by entering a username and password.
   - Existing users can log in with their credentials.

4. **Analyze Data**:
   - Use the "Plot Bar Graph" button to see data usage as a bar graph.
   - Use the "Plot Pie Chart" button to see data distribution as a pie chart.
   - Use the "Show Data" button to view raw data in a tabular format.

---

## Project Structure

- **data_usage_analyzer.py**: Main application script.
- **Internet-Data-Usage.csv**: Data file containing internet usage details.

---

## Future Enhancements
- **Encryption**: Encrypt user passwords for enhanced security.
- **Advanced Analysis**: Add more visualization options and metrics.
- **Cloud Integration**: Store data and user credentials on a cloud-based database.

---

## License
This project is licensed under the MIT License. Feel free to use and modify the code as needed.

---

## Acknowledgments
- Python and its libraries for simplifying data analysis and GUI development.
- MySQL for database management.
- The open-source community for inspiration and guidance.

