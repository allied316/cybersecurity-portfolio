### Burp Suite (Web Proxy & Interception)

## What is Burp Suite?
Burp Suite is a web application security testing tool that works as a man-in-the-middle proxy between your browser and a target website.
it allows you to:
    - Intercept requests
    - Modify parameters
    - Replay traffic
    - Discover vulnerabilities

## Core components
Intercept           Capture and modify requests before sending 
Repeater            Manually resend requests with changes
Target              Maps the application structure
Proxy               Handles browser <-> server traffic

## Common Use cases
- Modify login parameters
- Change cookies and headers
- Test for IDOR, auth bypass, SQLi 
- Analyze form requests

## Example Workflow
1. Set browser proxy to Burp (127.0.0.1:8080)
2. Turn Intercept ON
3. Visit target site
4. Capture request
5. Modify parameter
6. Forward to server
7. Observe response
