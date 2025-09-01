# Unity WebGL iframe Communication Test

This project demonstrates how to set up and test communication between a parent webpage and a Unity WebGL build inside an iframe.

## Folder Structure
```
testwebgl/
├── parent.html        # Parent page that hosts the iframe
├── Unity/            # Directory containing Unity WebGL build
│   └── index.html    # Unity WebGL page
└── README.md         # This file
```

## Local Testing Setup

### 1. Start a Local Web Server
You have two options:

#### Using Python's built-in server
```bash
# If you have Python installed, run:
python -m http.server 8000
```

#### Using VS Code Live Server
1. Install the "Live Server" extension in VS Code
2. Right-click on `parent.html`
3. Select "Open with Live Server"

### 2. Access the Test Page
- Open your browser and navigate to `http://localhost:8000/parent.html`
- Open browser DevTools (F12)
- Watch the console for communication messages

## Testing Workflow
1. Messages will appear in both the browser console and Unity frame
2. You can test the messaging system without waiting for Unity builds
3. Debug data being sent and received in real-time
4. Quickly iterate on the communication logic

## Important Notes
- Using `file://` protocol won't work with iframes, always use a local web server
- Check browser console for any potential errors or messages
- Make sure both parent and iframe pages have proper communication handlers set up

Once the local testing setup works, you can apply the same logic to your actual Unity WebGL build.
