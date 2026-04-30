# Talk to Your Data 🗣️📊

An AI-powered data analysis tool that allows you to query CSV files using natural language and get instant insights with generated Python code, SQL queries, and visualizations.

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Django](https://img.shields.io/badge/Django-5.1-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

## ✨ Features

### 🎯 Core Capabilities
- **Natural Language Queries** - Ask questions in plain English
- **Multi-Format Output** - View results in three tabs:
  - 📊 **Output** - Query results with automatic charts
  - 🐍 **Python Code** - Generated pandas code
  - 💾 **SQL Command** - Equivalent SQL query
- **One-Click Copy** - Copy any content with a single click
- **CSV Export** - Download query results
- **Smart Suggestions** - Get suggested questions based on your data
- **Query History** - Track your previous queries

### 📈 Visualization
- Automatic chart generation for appropriate queries
- Supports bar charts, scatter plots, and histograms
- Beautiful, responsive visualizations using Matplotlib and Seaborn

### 🤖 AI-Powered
- Uses Google Gemini 2.5 Flash for code generation
- Generates both Python/pandas and SQL queries
- Intelligent query understanding and execution

## 🚀 Quick Start

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)
- Google Gemini API key

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd talk_to_your_data
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   
   # On Windows
   venv\Scripts\activate
   
   # On macOS/Linux
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**
   
   Create a `.env` file in the root directory:
   ```env
   GEMINI_API_KEY=your_gemini_api_key_here
   ```

5. **Run database migrations**
   ```bash
   python manage.py makemigrations
   python manage.py migrate
   ```

6. **Start the development server**
   ```bash
   python manage.py runserver
   ```

7. **Open your browser**
   
   Navigate to `http://localhost:8000/`

## 📖 Usage

### Basic Workflow

1. **Upload CSV File**
   - Click "Upload CSV" button
   - Select your CSV file
   - File is automatically loaded

2. **Ask Questions**
   - Type your question in plain English
   - Examples:
     - "What is the total revenue?"
     - "Show me the top 5 products by sales"
     - "What is the average price by category?"
     - "Compare sales across regions"

3. **View Results**
   - **Output Tab**: See query results and charts
   - **Python Code Tab**: View generated pandas code
   - **SQL Command Tab**: See equivalent SQL query

4. **Export Data**
   - Use "Copy" buttons to copy content
   - Click "Download CSV" to export results

### Example Queries

```
"What is the total revenue?"
"Show me the top 10 customers by sales"
"What is the average order value?"
"Compare sales by region"
"Show the distribution of prices"
"Which products have sales above 1000?"
"Group sales by month"
```

## 🏗️ Project Structure

```
talk_to_your_data/
├── query_app/              # Main Django app
│   ├── models.py          # Database models
│   ├── views.py           # View logic and AI integration
│   ├── urls.py            # URL routing
│   └── templates/         # HTML templates
│       └── query_app/
│           └── index.html # Main interface
├── talk_to_your_data/     # Django project settings
│   ├── settings.py        # Project configuration
│   └── urls.py            # Root URL configuration
├── manage.py              # Django management script
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (create this)
└── README.md             # This file
```

## 🛠️ Technology Stack

### Backend
- **Django 5.1** - Web framework
- **Python 3.8+** - Programming language
- **Pandas** - Data manipulation
- **Google Gemini API** - LLM for code generation
- **Matplotlib & Seaborn** - Visualization

### Frontend
- **HTML5** - Structure
- **CSS3** - Styling with modern design
- **Vanilla JavaScript** - Interactivity
- **No external CSS frameworks** - Custom, lightweight design

### Database
- **SQLite** - Default Django database
- **Django ORM** - Database abstraction

## 📦 Dependencies

Key packages (see `requirements.txt` for complete list):
- `django>=5.1`
- `pandas>=2.0.0`
- `google-generativeai>=0.3.0`
- `python-dotenv>=1.0.0`
- `matplotlib>=3.7.0`
- `seaborn>=0.12.0`

## 🔧 Configuration

### Environment Variables

Create a `.env` file with:
```env
GEMINI_API_KEY=your_api_key_here
DEBUG=True  # Set to False in production
SECRET_KEY=your_secret_key_here  # Optional, Django will generate one
```

### Getting a Gemini API Key

1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Sign in with your Google account
3. Create a new API key
4. Copy the key to your `.env` file

## 🎨 Features in Detail

### Tabbed Interface
- **Output Tab**: Query results with automatic visualizations
- **Python Code Tab**: See the generated pandas code with syntax highlighting
- **SQL Command Tab**: View the equivalent SQL query

### Copy Functionality
- One-click copy buttons on all tabs
- Visual feedback ("✅ Copied!")
- Clipboard API integration

### Chart Generation
- Automatically detects when visualization is appropriate
- Supports multiple chart types:
  - Bar charts for categorical data
  - Scatter plots for numeric relationships
  - Histograms for distributions
- Clean, professional styling

### Query History
- Sidebar shows recent queries
- Click any query to re-run it
- Persistent across sessions

## 🔒 Security Notes

- Never commit your `.env` file to version control
- Keep your Gemini API key secure
- Set `DEBUG=False` in production
- Use environment-specific settings for deployment

## 🐛 Troubleshooting

### Common Issues

**"No module named 'google.generativeai'"**
```bash
pip install google-generativeai
```

**"GEMINI_API_KEY not found"**
- Ensure `.env` file exists in root directory
- Check that `GEMINI_API_KEY` is set correctly

**Database errors**
```bash
python manage.py makemigrations
python manage.py migrate
```

**Port already in use**
```bash
# Use a different port
python manage.py runserver 8001
```

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Support

For issues and questions, please open an issue on the GitHub repository.
