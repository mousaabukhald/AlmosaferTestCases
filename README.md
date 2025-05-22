
# 🧪 Almosafer Automation Test Suite

This project is a Selenium WebDriver automation test suite developed using **Java** and **TestNG** to test functionalities on the [Almosafer](https://www.almosafer.com) travel booking platform.

## 📁 Package Structure

```

TestCase.Almosafer
├── AppTest.java         // Main test class containing test methods
└── DataTestCases.java   // Data class with test data and configurations

```

---

## 🚀 Getting Started

### 🔧 Requirements

- Java JDK 8+
- Maven or any build tool (optional)
- TestNG
- Selenium WebDriver
- Chrome Browser
- ChromeDriver (configured in your system path)

---

## ✅ Test Descriptions

### `@BeforeTest` - Setup

- Navigates to the Almosafer English homepage
- Maximizes browser window

---

### Test Methods (`AppTest.java`)

| Priority | Method                  | Description                                                                 | Enabled |
|---------:|--------------------------|-----------------------------------------------------------------------------|:-------:|
| 1        | `ChesckTheLanguage()`    | Verifies if the default language is English (`en`)                         | ❌      |
| 2        | `CheckDefultCurrency()`  | Verifies if the default currency is **SAR**                                 | ❌      |
| 3        | `CheckPhoneNumber()`     | Verifies the displayed phone number (WhatsApp link)                         | ❌      |
| 4        | `QitafLogo()`            | Checks if the Qitaf logo is displayed in the footer                         | ❌      |
| 6        | `CheckingFlightDeparture()` | Verifies the default flight departure date (tomorrow)                     | ❌      |
| 7        | `CheckingFlightReturn()`   | Verifies the default flight return date (day after tomorrow)              | ❌      |
| 8        | `CheckHotelTab()`        | Checks whether the "Hotels" tab is selected by default                     | ❌      |
| 9        | `CahngeTheLanguage()`     | Randomly switches between English and Arabic interfaces                    | ❌      |
| 10       | `hotelSearch()`          | Performs a full hotel search based on random city and room options         | ✅      |
| 11       | `PageFullyLoaded()`      | Verifies the search results are fully loaded by checking visible text      | ✅      |

---

### `DataTestCases.java`

Holds data and configuration variables used by `AppTest`, including:

- ✅ Language URLs
- ✅ Expected strings: currency, phone number, date formats
- ✅ Randomized city selection (English and Arabic)
- ✅ Randomized hotel room options
- ✅ Calculated dates for departure and return (using `LocalDate.now()`)

---

## 🧪 Example Test Logic: `hotelSearch()`

- Clicks the Hotels tab
- Chooses a city (in Arabic or English based on site language)
- Clicks the Search button
- Chooses a random hotel room configuration
- Clicks final search to view hotel results

---

## 🛠 Technologies Used

- **Java**
- **Selenium WebDriver**
- **TestNG**
- **ChromeDriver**
- **Maven (optional)**

---

## 📸 Screenshot Automation

You can add support for screenshot capturing on failure using TestNG Listeners and `TakesScreenshot`.

---

## 📝 Notes

- All test cases are currently **disabled by default** except hotel search and page verification.
- You can enable them by setting `enabled = true` on each test method.
- Test data is dynamically generated, making each run slightly different.

---

## 📌 Author

Developed by **Mousa AbuKhaled**  
Feel free to contact or fork the project for enhancements.

---

## 📜 License

This project is open-source and available for free use in educational or testing contexts.

```

