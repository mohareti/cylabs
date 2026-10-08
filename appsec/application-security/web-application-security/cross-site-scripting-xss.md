# Cross Site Scripting (XSS)

**Cross-Site Scripting (XSS)** is a type of web security vulnerability that allows attackers to inject malicious scripts into web pages viewed by other users. XSS occurs when a web application includes untrusted data in a web page sent to the user without proper validation or escaping, enabling the attacker's code to run within the context of the victim's browser. XSS attacks can lead to the theft of sensitive data, session hijacking, or defacement of websites.

There are three primary types of XSS attacks:

1. **Stored XSS (Persistent XSS):** In this type of attack, the malicious script is permanently stored on the target server, often in a database or file, and then served to users who access a particular page. Examples include injecting a malicious script into a comment or forum post.
2. **Reflected XSS:** In this attack, the malicious script is embedded in a URL or a form input and is reflected off the web server. When a user clicks on a malicious link or submits a form, the script executes in the victim's browser and can steal their data or perform actions on their behalf. This type of XSS attack doesn't persist on the server and is often used in phishing attacks.
3. **DOM-based XSS:** This type of XSS occurs when the client-side scripts manipulate the Document Object Model (DOM) to execute the malicious code. Unlike the server-side XSS attacks, DOM-based XSS doesn't involve communication with the server. The attacker can manipulate the page's existing JavaScript code or DOM to execute the malicious script.

Here are examples of each type of XSS attack:

**Stored XSS (Persistent XSS):** Imagine a web application that allows users to post comments on a blog. If the application doesn't properly sanitize user input, an attacker can inject a malicious script into a comment like this:

```html
<script>
  // Malicious code to steal user cookies and send them to the attacker's server
  var cookies = document.cookie;
  // Send cookies to attacker's server
  // ...
</script>
```

When other users view the page with this comment, their browsers will execute the malicious script, potentially allowing the attacker to steal their cookies.

**Reflected XSS:** In a reflected XSS attack, an attacker may craft a malicious URL like this:

```text
https://example.com/search?query=<script>alert("XSS")</script>
```

When a user clicks on the link, the script is executed in their browser, showing an alert with the message "XSS."

**DOM-based XSS:** Consider a web page with the following JavaScript code that displays a message based on user input:

```javascript
function displayMessage() {
  var message = document.getElementById('message').value;
  document.getElementById('output').innerHTML = message;
}
```

An attacker could manipulate the URL to inject a script:

```text
https://example.com/page.html#<img%20src=x%20onerror=alert('XSS')>
```

When a user loads this URL, the attacker's script gets executed due to improper handling of the `#` fragment in the JavaScript code.

To prevent XSS attacks, web developers should implement proper input validation, output encoding, and security mechanisms like Content Security Policy (CSP). Additionally, security testing, code reviews, and vulnerability scanners can help identify and mitigate XSS vulnerabilities in web applications.
