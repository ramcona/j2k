# JSON to Kotlin Converter

A web-based tool that converts JSON objects into Kotlin data classes. This converter supports nested objects, arrays, and can optionally implement Android's Parcelable interface.

## Try It Online

🚀 Live Demo: [https://j2k.technice.id](https://j2k.technice.id)

## Features

- Convert JSON to Kotlin data classes
- Support for nested objects and arrays
- Optional Parcelable implementation for Android
- Automatic type inference
- Conversion history management
- Copy to clipboard functionality
- Download generated code as .kt file
- Responsive design for all devices

## Usage

1. **Enter Class Name**
   - Input the desired name for your main Kotlin class
   - Class names should follow Kotlin naming conventions (PascalCase)

2. **Input JSON**
   - Paste your JSON data into the input textarea
   - The JSON must be valid and properly formatted

3. **Parcelable Option**
   - Check the "Implement Parcelable" box if you need Android Parcelable implementation
   - This is useful for passing data between Android components

4. **Convert**
   - Click the "Convert" button to generate Kotlin classes
   - The tool will automatically create nested classes as needed

5. **Generated Code Options**
   - Copy: Click the clipboard button to copy the generated code
   - Download: Save the generated code as a .kt file

## Conversion Features

- Supports primitive types (String, Int, Double, Boolean)
- Handles nullable values
- Converts JSON objects to nested Kotlin classes
- Converts arrays to ArrayList<T>
- Handles maps with dynamic keys
- Implements Serializable by default
- Optional Parcelable implementation

## History Management

- Automatically saves the last 10 conversions
- Click on any history item to restore its content
- Delete individual history items
- Clear entire history with one click
- Displays timestamp for each conversion

## Type Conversion Rules

| JSON Type | Kotlin Type |
|-----------|-------------|
| String | String |
| Number (Integer) | Int |
| Number (Decimal) | Double |
| Boolean | Boolean |
| Object | Custom Class |
| Array | ArrayList<T> |
| null | String? |
| Map-like object | Map<String, T> |

## Code Sample

```json
{
  "name": "John",
  "age": 30,
  "address": {
    "street": "123 Main St",
    "city": "New York"
  }
}
```

Converts to:

```kotlin
class Person : Serializable {
    var name: String = ""
    var age: Int = 0
    var address: Address = Address()
}

class Address : Serializable {
    var street: String = ""
    var city: String = ""
}
```

## Browser Compatibility

- Chrome (recommended)
- Firefox
- Safari
- Edge
- Modern mobile browsers

## Dependencies

- Bootstrap 5.3.0
- No backend required - runs entirely in the browser

## Local Development

1. Clone the repository
2. Open `index.html` in a web browser
3. No build process or server required

## License

© 2025 JSON to Kotlin Converter. All Rights Reserved.
