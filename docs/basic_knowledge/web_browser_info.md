## What is a User-Agent?

A **User-Agent** is an **HTTP request header** that identifies the client (browser, application, or tool) sending the request to a web server.

### Simple Definition

> **A User-Agent tells the web server which browser, operating system, or application is making the request.**

### Example

```text
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64)
Chrome/137.0.0.0 Safari/537.36
```

This tells the server that the request is coming from:

* **Browser:** Chrome
* **Operating System:** Windows 10
* **Platform:** 64-bit

## Why is User-Agent Important?

* Identifies the browser or application.
* Helps websites display compatible content.
* Used in web server logs for monitoring.
* Helps SOC analysts detect suspicious or automated traffic.
* Can reveal tools like `curl`, `sqlmap`, `Nmap`, or `python-requests`.
* Helps distinguish normal users from bots or scripts.

## SOC Analyst Interview Answer

> **A User-Agent is an HTTP request header that identifies the client's browser, operating system, or application. It is important because it helps identify the source of web requests, detect automated tools, investigate suspicious activity, and analyze web server logs.**

**Note:** A User-Agent can be **spoofed (faked)**, so it should always be analyzed along with the source IP, request pattern, and other log data.



## Common (Legitimate) User-Agents
Common User-Agents are strings sent by normal web browsers like Chrome, Firefox, Edge, and Safari when a user visits a website. They help the server identify the browser and operating system being used.

| Browser         | Developer            | Rendering Engine | Platform                            | Best For                 |
| --------------- | -------------------- | ---------------- | ----------------------------------- | ------------------------ |
| Google Chrome   | Google               | Blink            | Windows, macOS, Linux, Android, iOS | Speed, extensions        |
| Mozilla Firefox | Mozilla              | Gecko            | Windows, macOS, Linux, Android, iOS | Privacy, open source     |
| Microsoft Edge  | Microsoft            | Blink            | Windows, macOS, Android, iOS        | Windows integration      |
| Safari          | Apple                | WebKit           | macOS, iPhone, iPad                 | Apple ecosystem          |
| Opera           | Opera                | Blink            | Windows, macOS, Linux, Android, iOS | Built-in VPN, ad blocker |
| Brave           | Brave Software       | Blink            | Windows, macOS, Linux, Android, iOS | Privacy and ad blocking  |
| Vivaldi         | Vivaldi Technologies | Blink            | Windows, macOS, Linux, Android      | Customization            |
| Tor Browser     | The Tor Project      | Gecko            | Windows, macOS, Linux, Android      | High anonymity           |


## Common User-Agents Used by Security Tools or Attackers
Below is a list of common tools whose **default User-Agent** strings may appear in web server logs. These tools are used by attackers, penetration testers, and security professionals. Seeing one of these User-Agents **does not automatically mean an attack is occurring**.

| Tool            | Typical User-Agent             | Purpose                                      |
| --------------- | ------------------------------ | -------------------------------------------- |
| Nmap            | `Nmap Scripting Engine`        | Network scanning and service detection       |
| curl            | `curl/8.x.x`                   | Sending HTTP requests from the command line  |
| Wget            | `Wget/1.x`                     | Downloading web pages and files              |
| Python Requests | `python-requests/2.x`          | Python scripts and automation                |
| Go HTTP Client  | `Go-http-client/1.1`           | Go applications and automation               |
| Java            | `Java/17`                      | Java-based applications                      |
| PowerShell      | `PowerShell`                   | Windows automation and scripting             |
| sqlmap          | `sqlmap/1.x`                   | SQL injection testing                        |
| Nikto           | `Nikto/2.x`                    | Web server vulnerability scanning            |
| DirBuster       | `DirBuster`                    | Directory and file enumeration               |
| Gobuster        | `gobuster/3.x`                 | Directory, DNS, and virtual host enumeration |
| ffuf            | `ffuf/2.x`                     | Web fuzzing and content discovery            |
| Burp Suite      | `Burp Suite`                   | Web application testing and proxying         |
| OWASP ZAP       | `ZAP`                          | Web vulnerability scanning                   |
| Masscan         | `masscan`                      | High-speed port scanning                     |
| Nuclei          | `Nuclei - Open-source project` | Automated vulnerability scanning             |
| httpx           | `httpx/x.x`                    | HTTP probing and reconnaissance              |

## Important SOC Analyst Note

Attackers frequently **change or spoof** their User-Agent to look like a legitimate browser. For example:

```text
Mozilla/5.0 (Windows NT 10.0; Win64; x64)
AppleWebKit/537.36 (KHTML, like Gecko)
Chrome/137.0.0.0 Safari/537.36
```

This makes malicious traffic appear as if it came from a normal browser like Chrome.

## SOC Interview Answer

**Q: Which User-Agents are commonly observed during SOC investigations?**

**Answer:**

* Browser User-Agents (Chrome, Firefox, Edge, Safari)
* `curl`
* `Wget`
* `python-requests`
* `Go-http-client`
* `Java`
* `PowerShell`
* `Nmap Scripting Engine`
* `sqlmap`
* `Nikto`
* `Gobuster`
* `DirBuster`
* `ffuf`
* `Burp Suite`
* `OWASP ZAP`
* `Masscan`
* `Nuclei`

