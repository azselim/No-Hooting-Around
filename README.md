# No Hooting Around - Chrome Productivity Extension 🦉

A Chrome extension that helps users stay focused on their goals using an animated owl companion and AI-powered productivity tracking.

## Features

- **Goal Setting**: Users can set specific goals for their work/study sessions
- **Real-time Monitoring**: An AI-powered system analyzes webpage content to determine if users are staying on task
- **Animated Owl Companion**: A friendly owl companion provides visual feedback about productivity
- **Smart Redirection**: Automatically redirects users away from distracting content
- **Productivity Validation**: Users can justify their webpage visits when the system detects potential off-task behavior

## Technical Stack

- **Frontend**: HTML, CSS, JavaScript (Chrome Extension)
- **Backend**: Python with Flask
- **AI Integration**: OpenAI GPT-4 Vision API

## Installation

1. Clone the repository:
```bash
git clone "https://github.com/RohanT766/DeltaHacksXI"
```

2. Set up the backend:
```bash
# Create and activate a virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install flask openai flask-cors

# Set up environment variables
export OPENAI_API_KEY=your_api_key_here
```

3. Load the extension in Chrome:
   - Open Chrome and navigate to `chrome://extensions/`
   - Enable "Developer mode"
   - Click "Load unpacked"
   - Select the extension directory

## Usage

### Ensure the Backend is Running:
```bash
# Run the Flask server
python backend.py
```

1. Click the extension icon in Chrome
2. Enter your current work/study goal
3. Start working - the owl will monitor your activity
4. If you visit potentially distracting content:
   - For moderately off-task content: You'll be prompted to justify your visit
   - For clearly off-task content: You'll be redirected to your previous productive page

## Project Structure

```
├── backend.py           # Flask backend server
├── manifest.json        # Chrome extension manifest
├── popup.html          # Extension popup interface
├── popup.css           # Popup styles
├── popup.js            # Popup functionality
├── background.js       # Extension background script
├── content.js          # Page content script
└── .gitignore         # Git ignore file
```

## How It Works

1. **Goal Setting**: Users set their productivity goals through the extension popup
2. **Screenshot Analysis**: The extension periodically captures screenshots of active tabs
3. **AI Analysis**: Screenshots are analyzed by GPT-4 Vision to determine relevance to the user's goal
4. **Response System**:
   - 0-30% off-task: No intervention
   - 30-70% off-task: User prompted to justify their activity
   - 70-100% off-task: Automatic redirection to previous productive page

## License

MIT License

## Acknowledgments

- OpenAI for GPT-4 Vision API
- Giphy for owl animations
