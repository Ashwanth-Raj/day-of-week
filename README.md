# 📅 Day of the Week Finder

A simple web app that helps you find the day of the week for any given date using Zeller's Congruence formula.

## 🔍 Features

- Input any valid date (DD-MM-YYYY format)
- Calculates the corresponding weekday
- Validates input to avoid incorrect dates
- Uses only HTML, CSS, and JavaScript
- Clean, responsive user interface
- No external dependencies required

## 🚀 How to Use

1. Clone or download this repository:
   ```bash
   git clone https://github.com/yourusername/day-of-week-finder.git
   ```

2. Open the `index.html` file in your browser.

3. Enter the date components:
   - **Day** (1–31)
   - **Month** (1–12)
   - **Year** (e.g., 2025)

4. Click the **Find Day** button

5. The corresponding weekday will be displayed!

## 🧠 How It Works

This app uses **Zeller's Congruence** algorithm, which calculates the day of the week for any Gregorian date.

### The Formula

```javascript
let h = (day + Math.floor((13 * (month + 1)) / 5) + K + Math.floor(K / 4)
         + Math.floor(J / 4) + 5 * J) % 7;
```

Where:
- `K = year % 100` (year of the century)
- `J = Math.floor(year / 100)` (zero-based century)
- `day` = day of the month
- `month` = adjusted month (March = 1, April = 2, ..., February = 12)

### Result Mapping

The result `h` maps to weekdays as follows:
- `0` = Saturday
- `1` = Sunday
- `2` = Monday
- `3` = Tuesday
- `4` = Wednesday
- `5` = Thursday
- `6` = Friday


## 💻 Technologies Used

- **HTML5** - Structure and layout
- **CSS3** - Styling and responsive design
- **JavaScript (ES6+)** - Logic and DOM manipulation

## 🎯 Example Usage

**Input:**
- Day: 31
- Month: 5
- Year: 2025

**Output:** Saturday

## 🔧 Customization

You can easily customize the app by:
- Modifying the CSS for different themes
- Adding date range restrictions
- Including additional date formats
- Adding animations or transitions

## 📝 Algorithm Notes

Zeller's Congruence treats January and February as months 13 and 14 of the previous year. This adjustment is handled automatically in the code.

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

⭐ **Star this repository if you found it helpful!**
