---
name: Bug report
about: Something is not working, not working as intended, or else
title: "[Bug]"
labels: bug
assignees: DeadlyFirex

---

**Describe the Bug**  
[Provide a detailed description of the bug. Include what triggers the bug and its effects on the system.]  

[Example: "Causing a connection to `keep-alive` will result in the application not consuming the request body on `PUT`, `DELETE`, and `POST`. This occurs when a request exits prematurely (e.g., due to bad input), causing the `{}` body to pass to the next request and creating malformed responses or internal issues."]  

---

**Steps to Reproduce**  
[Provide a step-by-step guide to reproduce the issue. Include all necessary configuration or setup details.]  

1. [Step 1: E.g., Start the application with proper configuration.]  
2. [Step 2: E.g., Send requests to endpoints requiring a request body.]  
3. [Step 3: E.g., Ensure the requests include `keep-alive`.]  
4. [Step 4: E.g., Send invalid data, forcing the endpoint to exit prematurely.]  

---

**Expected Behavior**  
[Describe what you expect to happen when the system works correctly.]  

[Example: "The request body should be consumed and not passed to subsequent requests."]  

---

**Actual Behavior**  
[Describe what actually happens when the bug occurs.]  

[Example: "The `{}` body gets passed to the next request, causing internal issues or malformed responses."]  

---

**Screenshots**  
[If applicable, include screenshots or logs that help illustrate the issue.]  
[Attach or describe relevant visuals here.]  

---

**Operating System**  
[List the operating system and version where the issue was observed, or mark as "N/A" if not OS-dependent.]  

[Example: "N/A (non-OS dependent)."]  

---

**Additional Context**  
[Provide any additional details, notes, or references that help clarify the issue.]  

[Example:  
"When setting the request body to `{}` using Postman or another HTTP client, the first request returns a 200 status, while the second returns a 405 error. Logs show the request method as `{}`POST.  
This issue does not occur when running a production WSGI server (e.g., `gunicorn`). Closing the connection while using the development server avoids the issue. See related discussion: https://github.com/pallets/flask/issues/4507."]  

---

**Workarounds**  
[Include any known workarounds or temporary fixes, if applicable.]  

[Example: "Running a production WSGI server like `gunicorn` or closing the connection in development resolves the issue."]  

---

**Related Issues**  
[List any related issues or discussions for additional context.]  

- Related-to: [Insert related issue or discussion link here]  
- Related-to: [Insert related issue or discussion link here]
