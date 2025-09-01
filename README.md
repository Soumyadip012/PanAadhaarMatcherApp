# PanAadhaarMatcherApp

A simple **Java-based CLI application** to validate and match names across **PAN and Aadhaar datasets**.  
This tool can be useful for **identity verification, duplicate detection, and compliance checks** where PAN and Aadhaar records need to be compared.

---

## 🚀 Features

- **Name Matching** – Compares PAN and Aadhaar names for exact or near matches.  
- **Fuzzy Matching Support** – Handles small variations (case sensitivity, spacing, minor typos).  
- **CLI Based** – Lightweight and easy to run from the terminal.  
- **Extensible** – Can be extended for advanced similarity algorithms (Levenshtein, Soundex, etc.).

---

## 📂 Project Structure

PanAadhaarMatcherApp/
├── src/
│ └── main/java/com/panaadhaar/
│ ├── Main.java # CLI entry point
│ └── Matcher.java # Core matching logic
├── .gitignore
├── README.md
└── PanAadhaarMatcherApp.iml

yaml
Copy
Edit

---

## 🛠️ Getting Started

### Prerequisites
- **Java JDK 8+** installed  
- (Optional) **Maven/Gradle** if you want to manage builds

### Run Locally

1. **Clone the repository**
   ```bash
   git clone https://github.com/Soumyadip012/PanAadhaarMatcherApp.git
   cd PanAadhaarMatcherApp
Compile the code

bash
Copy
Edit
javac -d out src/main/java/com/panaadhaar/*.java
Run the application

bash
Copy
Edit
java -cp out com.panaadhaar.Main <pan_file> <aadhaar_file>
Example:

bash
Copy
Edit
java -cp out com.panaadhaar.Main pan.csv aadhaar.csv
⚙️ How It Works
Input Files – Reads PAN and Aadhaar datasets (CSV/TXT).

Normalization – Cleans and standardizes names (removes case/whitespace issues).

Matching – Performs:

Exact match

Fuzzy match (string similarity)

Result – Prints matched/unmatched records with status.

🧾 Example Output
yaml
Copy
Edit
Comparing PAN and Aadhaar records...

Match Found:
- PAN: "SOUMYADIP KUNDU"
- Aadhaar: "Soumyadip Kundu"
Status: ✔ Likely Match

------------------------------
Total Records: 10
Matched: 9
Unmatched: 1
🔮 Future Enhancements
Support for JSON/Excel/database inputs

Advanced fuzzy matching algorithms (Levenshtein, Cosine Similarity)

Add a GUI/Web Interface for non-technical users

Integration with Aadhaar/PAN APIs for live verification
