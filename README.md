# Price Tampering Vulnerability Assessment – Odgmart.com
**📌 Project Overview**
> This project focuses on identifying and analyzing **price tampering vulnerabilities** in the ```Odgmart.com``` web application through **authorized and ethical security testing.**

The objective is to evaluate whether the application properly validates pricing data on the **server side** during the transaction and checkout process, and to understand the risks associated with trusting client-side input.

**🎯 Objectives**
- Identify price tampering vulnerabilities in a web application
- Analyze client–server communication during checkout
- Understand the impact of insufficient server-side validation
- Recommend secure development practices to prevent price manipulation

**🛠️ Tools & Technologies**
- Google Chrome
- Burp Suite
- Burp Suite Browser Extension
- FoxyProxy Extension
- HTTP/HTTPS Protocol Analysis

**🔍 Methodology**

**Step 1**

> Access the website ```www.ogdmart.com```
 using ```Google Chrome with the Burp Suite extension enabled```` to monitor HTTP requests.

**Step 2**

> Select a product and enter the required details such as ```PIN code``` and ```delivery date.```

**Step 3**

> Add the selected product to the cart and fill in user details including ```name and address``` during checkout.

**Step 4**

> Use ```Burp Suite``` to intercept and analyze client–server communication related to pricing.

**Step 5**

> Open ```Burp Suite → Proxy → Intercept``` to capture HTTP requests generated during the checkout process.

**Step 6**

> Enable the ```FoxyProxy extension``` in the browser to route all traffic through Burp Suite.

**Step 7**

> Analyze the intercepted ```POST request``` and modify the price value
(e.g., change ```₹1599 to ₹15```) to test whether the application accepts manipulated pricing data.

**Step 8**

> Disable interception, forward the modified request to the server, and observe the application response to confirm whether price tampering is successful.

**⚠️ Vulnerability Description**

> ```Price Tampering ```is a high-severity vulnerability that occurs when a web application trusts client-side price values instead of validating them on the server.

If exploited, attackers can:

- Purchase products at significantly reduced prices
- Cause direct financial loss
- Compromise the integrity of business transactions

**✅ Conclusion**

> Price tampering vulnerabilities arise due to the lack of ```server-side price validation.``` Applications must never rely on client-controlled values for critical parameters such as price.

**Recommended Mitigations:**
- Implement strict s```erver-side price validation```
- Use secure session and transaction controls
- Recalculate prices on the server before payment processing
- Apply integrity checks and logging mechanisms

**📄 Disclaimer**
>This project was conducted strictly for ```educational and ethical purposes.```
All testing was performed in a controlled environment without causing harm or unauthorized impact
