# Mobile Radio Frequency Spectrum Analyzer

A simple web-based tool for visualizing and analyzing mobile radio frequency spectrum, designed for FM frequencies in the 446.0 - 446.2 MHz range (but flexible for other frequencies).

## Features

- Add and manage radio frequencies with custom names
- Support for both narrowband (12.5 kHz) and wideband (25 kHz) FM emissions
- Visual spectrum chart showing frequency ranges
- Automatic overlap detection (distinguishes between adjacent and overlapping frequencies)
- JSON import/export functionality
- Local storage persistence
- Mobile-responsive design

## Usage

Simply open the `index.html` file in your web browser, or visit the live demo:

[Live Demo](https://dusansimic.github.io/frequency-spectrum/)

## How to Use

1. Enter a name/label for your frequency (e.g., "Channel 1", "Security Team")
2. Enter the frequency in MHz (e.g., 446.00625)
3. Select the bandwidth (Narrowband 12.5 kHz or Wideband 25 kHz)
4. Click "Add Frequency" or press Enter
5. View your frequencies in the list and on the spectrum chart
6. Export your configuration as JSON or import a previously saved file

## JSON Format

The tool uses the following JSON format for storing and exporting frequencies:

```json
[
  {
    "_id": 1234567890,
    "name": "Channel 1",
    "frequency": 446006250,
    "mode": "NFM"
  },
  {
    "_id": 1234567891,
    "name": "Security Team",
    "frequency": 446018750,
    "mode": "FM"
  }
]
```

**Field descriptions:**
- `_id`: Unique identifier (integer timestamp)
- `name`: Display name for the frequency (string)
- `frequency`: Frequency in Hz as an integer (e.g., 446006250 = 446.00625 MHz)
- `mode`: Emission mode - `"FM"` for wideband (25 kHz) or `"NFM"` for narrowband (12.5 kHz)

The tool automatically migrates old format files during import.

## License

BSD 2-Clause License - See [LICENSE](LICENSE) file for details.
