# Cross-Site Request Forgery (CSRF)

**CSRF (Cross-Site Request Forgery)** is a web security vulnerability that occurs when an attacker tricks a user into unknowingly making an unwanted, malicious request to a different website on which the user is authenticated. CSRF attacks exploit the trust that a website has in a user's browser, making it seem like the user is making legitimate requests when, in fact, they are manipulated by the attacker.

There are two primary types of CSRF attacks:

1. **Stored CSRF (Persistent CSRF):**
   * In a stored CSRF attack, the attacker manages to store a malicious request on a website where it can be later executed when an unsuspecting user visits a page.
   * **Example:** Consider an attacker who posts a malicious link on a forum. When a logged-in user clicks the link, their session cookie authenticates the request, and they unwittingly perform an action on a different site, such as changing their email address or password.
2. **Reflected CSRF (Non-persistent CSRF):**
   * In a reflected CSRF attack, the attacker sends the victim a malicious link, and the victim's browser sends an unauthorized request as a result of clicking the link. The request often carries parameters that are included in the URL.
   * **Example:** An attacker sends an email to a victim with a link like `https://example.com/action?param=value`. When the victim clicks the link, the action is performed on their behalf, as they are already authenticated in the target site.

Here's a simplified example of a CSRF attack:

1. **Scenario:**
   * Alice is logged into her online banking account.
   * The bank's website has a feature that allows users to change their email address.
2. **Attack Steps:**
   * The attacker, Eve, creates a malicious website with an HTML form that submits a request to change the email address on the bank's website when the victim loads it.
   * Eve sends Alice an email containing a link to her malicious website.
3. **Execution:**
   * Alice receives the email and clicks the link.
   * Her browser loads Eve's website, which in turn submits a request to change Alice's email address on the bank's website.
   * Since Alice is already authenticated with the bank, the request goes through without her consent.
4. **Outcome:**
   * Alice's email address is changed to the attacker's address, locking her out of her own account.

To prevent CSRF attacks, web applications should implement anti-CSRF measures, such as using unique tokens for each user session and requiring these tokens to be included in any sensitive requests. This ensures that only legitimate requests from the same user session are allowed to modify data or perform actions on the server.
