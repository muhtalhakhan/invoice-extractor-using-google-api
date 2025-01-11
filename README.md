# Invoice Extractor using Google API

This repository contains a Python-based project that extracts information from invoices using Google's Vision API. The project is designed to automate the process of extracting key details from invoices, such as invoice number, date, total amount, and vendor information, by leveraging Optical Character Recognition (OCR) capabilities provided by Google Cloud.

## Features

- **OCR Processing**: Utilizes Google Vision API to extract text from uploaded invoice images or PDFs.
- **Data Extraction**: Parses the extracted text to identify and retrieve key invoice details.
- **Output**: Generates structured data (e.g., JSON) containing the extracted information.
- **Easy Integration**: Simple setup and integration with Google Cloud services.

## Prerequisites

Before you begin, ensure you have the following:

- **Google Cloud Account**: You need a Google Cloud account to access the Vision API.
- **Google Cloud Project**: Create a project in the Google Cloud Console.
- **Service Account Key**: Generate a service account key and download the JSON file. This will be used to authenticate your requests to the Google Vision API.
- **Python 3.x**: Ensure you have Python 3.x installed on your system.
- **Google Cloud SDK**: Install the Google Cloud SDK and authenticate using your Google account.

## Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/muhtalhakhan/invoice-extractor-using-google-api.git
   cd invoice-extractor-using-google-api
   ```

2. **Set Up Virtual Environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set Up Google Cloud Credentials**:
   - Place your Google Cloud service account JSON key in the project directory.
   - Set the environment variable `GOOGLE_APPLICATION_CREDENTIALS` to point to your service account key:
     ```bash
     export GOOGLE_APPLICATION_CREDENTIALS="path/to/your/service-account-file.json"
     ```

## Usage

1. **Run the Script**:
   ```bash
   python main.py --input path/to/your/invoice.pdf
   ```

   Replace `path/to/your/invoice.pdf` with the path to your invoice file (PDF or image).

2. **View the Output**:
   The script will output the extracted invoice details in JSON format. The output will include fields such as:
   - `invoice_number`
   - `invoice_date`
   - `total_amount`
   - `vendor_name`
   - `vendor_address`

   Example Output:
   ```json
   {
       "invoice_number": "INV-12345",
       "invoice_date": "2023-10-01",
       "total_amount": "$1,200.00",
       "vendor_name": "Example Corp",
       "vendor_address": "123 Example St, Example City, EX 12345"
   }
   ```

## Configuration

You can customize the script by modifying the `config.py` file. This file contains settings such as:

- **Language Hints**: Specify the language hints for better OCR accuracy.
- **Output Format**: Customize the output format (e.g., JSON, CSV).

## Contributing

Contributions are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request.

1. **Fork the Repository**
2. **Create a New Branch**:
   ```bash
   git checkout -b feature/YourFeatureName
   ```
3. **Commit Your Changes**:
   ```bash
   git commit -m 'Add some feature'
   ```
4. **Push to the Branch**:
   ```bash
   git push origin feature/YourFeatureName
   ```
5. **Open a Pull Request**

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments

- **Google Cloud Vision API**: For providing powerful OCR capabilities.
- **Python Community**: For the extensive libraries and tools that made this project possible.

## Contact

For any questions or feedback, feel free to reach out:

- **Muhammad Talha Khan**: [GitHub Profile](https://github.com/muhtalhakhan)
- **Email**: [Shoot me your query](mailto:talhakhan325.work@gmail.com)

---

Thank you for using the Invoice Extractor using Google API! We hope this tool simplifies your invoice processing tasks.
