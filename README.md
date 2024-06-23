# Apple Stock Data Processor and Visualizer

## Project Description

This Python package processes and visualizes Apple stock data from a CSV file. The project includes functionalities to load, process, and visualize stock data. The primary goal is to compute statistics, clean data, filter based on average volume, aggregate weekly data, and visualize it using a candlestick chart.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Running the Main Script](#running-the-main-script)
  - [Data Processing](#data-processing)
    - [Initialize the DataProcessor and Load Data](#initialize-the-dataprocessor-and-load-data)
    - [Compute Statistics](#compute-statistics)
    - [Filter Data by Average Volume](#filter-data-by-average-volume)
    - [Add the Day of the Week](#add-the-day-of-the-week)
  - [Data Visualization](#data-visualization)
    - [Initialize the StockVisualizer with the Filtered Data](#initialize-the-stockvisualizer-with-the-filtered-data)
    - [Create and Display the Candlestick Chart](#create-and-display-the-candlestick-chart)
- [Running Tests](#running-tests)
- [Code Style](#code-style)
- [Possible Errors and Resolutions](#possible-errors-and-resolutions)
- [Contributing](#contributing)
- [License](#license)
- [Credits](#credits)
- [Author](#author)

## Prerequisites

- Python 3.7 or later installed on your system.
- pip (Python package installer).

## Installation

1. Clone the repository or download the package files.
2. Navigate to the project directory.

### Install Required Libraries

Ensure you have all the necessary libraries installed. You can install the dependencies individually:
```
pip install pandas plotly
```
### Package Installation
Navigate to the project directory and install the package using pip:
```
pip install dist/my_package-0.1.0-py3-none-any.whl
```
Alternatively, to install the .tar.gz file:

```
pip install dist/my_package-0.1.0.tar.gz
```
## Usage
### Running the Main Script
The main script (`main.py`) demonstrates the usage of the `DataProcessor` and `StockVisualizer` classes. It performs the following tasks:

1. Loads data from a CSV file.
2. Computes statistics.
3. Filters data by average volume.
4. Adds the day of the week to the data.
5. Aggregates data weekly.
6. Visualizes the data.

####
To run the main script, navigate to the project directory and execute:
```
python main.py
```
Make sure to update the `DATA_FILE_PATH` variable in `main.py` with the path to your CSV file.

## Data Processing
To manually use the `DataProcessor` for loading and processing data, follow these steps:

### Initialize the `DataProcessor` and Load Data
```
from my_package.data_processing import DataProcessor

DATA_FILE_PATH = 'path/to/your/data.csv'
processor = DataProcessor(DATA_FILE_PATH)
processor.load_data()
```

### Compute Statistics
```
max_value, min_value, average_value = processor.compute_statistics()
```

### Filter data by Average Volume
```
filtered_data = processor.filter_by_average_volume()
```
### Add the day of the week
```
data_with_day = processor.add_day_of_week()
```

## Data Visualization
To visualize the data using StockVisualizer, follow these steps:

### Initialize the `StockVisualizer` with the Filtered Data
```
from my_package.visualization import StockVisualizer

visualizer = StockVisualizer(filtered_data)
```
### Create and Display the Candlestick Chart
```
fig = visualizer.create_candlestick_chart()
fig.show()
```


## Running Tests
To ensure the package functions correctly, you can run the included tests using pytest.

### Install `pytest` if you haven't already:
```
pip install pytest
```
### Run the tests
```
pytest tests/
```


## Code Style
Adhere to PEP 8 guidelines and ensure code style consistency using `flake8` and `black`.

### Check for `PEP 8` Compliance
```
pip install flake8
flake8 src/ tests/
```

### Format Code Using `black`
```
pip install black
black src/ tests/
```
## Possible Errors and Resolutions

### Error: `ModuleNotFoundError`
#### Description: 
You might encounter this error if the package or one of its dependencies is not installed correctly.
#### Resolution:

Ensure all dependencies are installed by running:
```
pip install .
```

### Error: `ImportError`
#### Description: 
This error may occur if the module or function names are incorrect.

#### Resolution:

Check the import statements in your code to ensure they match the module and function names exactly.
Verify that the files are located in the correct directories.

### Error: `FileNotFoundError`
#### Description: 
This error occurs when the specified CSV file is not found.

#### Resolution:

Ensure the file path provided in `DATA_FILE_PATH` is correct.
Verify that the file exists at the specified location.


### Error: `ValueError`
#### Description: 
This error may occur during data processing if the data format is incorrect.

#### Resolution:

Check the CSV file to ensure it contains the expected columns and data types.
Validate the data before processing to handle any anomalies.

### Error: `AssertionError` (during tests)
#### Description: 
This error occurs when the tests fail due to unexpected results.

#### Resolution:

Review the test cases to understand the expected outputs.
Ensure the functions are working as intended by debugging with sample inputs.


## Contributing
Contributions are welcome! If you have any improvements or suggestions, please submit a pull request or open an issue on the GitHub repository.

## License
This project is licensed under the MIT License.

## Credits
* Data Source: Apple Inc. Stock Data
* Libraries Used: pandas, plotly

## Author
Praveen Thanniru

Email: praveenthanniru7@gmail.com

GitHub: https://github.com/praveen-thanniru

