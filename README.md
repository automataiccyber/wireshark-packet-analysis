# 🧪 Wireshark Packet Analysis

A beginner-friendly project that demonstrates how to use **Wireshark** to capture and analyze network traffic, including DNS queries, HTTP requests, and the detection of potential vulnerabilities like cleartext credentials.

---

## 📌 Project Goals

- Learn how to use Wireshark for network monitoring.
- Capture common types of traffic (DNS, HTTP).
- Identify insecure traffic patterns (e.g., unencrypted logins).
- Take annotated screenshots and document findings.

---

## 🧰 Tools Used

| Tool      | Purpose                            |
|-----------|------------------------------------|
| Wireshark | Network protocol analyzer          |
| Browser   | Generate web traffic               |
| Terminal  | Trigger DNS/ICMP events            |

---

## 🖥️ Environment Setup

- **Operating System**: Kali Linux
- **Network**: Local home network 
- **Test Sites**:  
  - `http://example.com`  
  - `http://neverssl.com` (HTTP-only)

---

## 🔎 Step-by-Step Guide

### 1. Start Capture
- Open Wireshark with admin privileges.
- Select your active network interface (e.g., Wi-Fi).
- Click **Start Capture**.

### 2. Generate Traffic
Open your terminal or browser and run the following:

```bash
ping example.com
nslookup example.com
````

Then in a browser:

* Visit `http://example.com`
* Visit `http://neverssl.com`

### 3. Stop and Save Capture

* Let the capture run for \~30 seconds.
* Stop the capture.
* Save the file as `traffic-analysis.pcapng`.

---

## 📊 Packet Analysis Summary

| Traffic Type | Wireshark Filter                | Observations                                  |
| ------------ | ------------------------------- | --------------------------------------------- |
| DNS Queries  | `dns`                           | Show domain resolution                        |
| HTTP GET     | `http.request`                  | Found plaintext headers                       |
| TCP Stream   | Right-click > Follow TCP Stream | View full HTTP session                        |

---

## 🖼️ Screenshots (Examples)

> * DNS query details

<img width="1919" height="807" alt="image" src="https://github.com/user-attachments/assets/44edeb34-04ea-4f9a-9c89-e9dacd36c687" />
<img width="1919" height="807" alt="image" src="https://github.com/user-attachments/assets/ebabe55d-de59-4a34-a26b-07d462728b88" />

> * HTTP GET request headers

<img width="1919" height="807" alt="image" src="https://github.com/user-attachments/assets/9d0822e6-973d-4b4a-88f5-512da947755f" />
<img width="1919" height="807" alt="image" src="https://github.com/user-attachments/assets/52355ed0-5594-4881-bd0c-141775b2e0e6" />

> * Full TCP stream analysis

<img width="1283" height="902" alt="image" src="https://github.com/user-attachments/assets/b60f650d-25ff-4259-b360-1901daa2e12c" />
<img width="1276" height="901" alt="image" src="https://github.com/user-attachments/assets/46a57dfd-09dc-4f2d-9c23-68dc5ae2d5a4" />
<img width="1276" height="902" alt="image" src="https://github.com/user-attachments/assets/ac750643-8cff-4718-872a-a1482c2c3dfd" />






---

## 🛡️ Security Observations

* DNS traffic exposes browsing habits.
* HTTP does not encrypt headers.
* Use HTTPS and secure protocols to prevent sniffing.

---

## ⚠️ Ethics & Legal Notice

> This project was conducted on a **controlled network** with full permission.
> Never sniff or capture traffic on networks without explicit authorization.

---

## 📁 Project Structure

```
wireshark-packet-analysis/
├── traffic-analysis.pcapng         # Sample capture file
├── screenshots/                    # Annotated screenshots
└── README.md                       # Project documentation
```

---

## ✅ What I Learned

* How to use display filters in Wireshark.
* How to follow a TCP stream to reconstruct HTTP sessions.
* How insecure protocols can leak sensitive information.

---

## 📚 References

* [Wireshark Filters Cheat Sheet](https://packetlife.net/media/library/23/Wireshark_Display_Filters.pdf)
* [Neverssl](http://neverssl.com)
* [Wireshark User Guide](https://www.wireshark.org/docs/wsug_html_chunked/)

```


- Pre-made screenshots
- To turn this into a structured GitHub repo (with folders and license)

I'm happy to help you make it look portfolio-ready.
```
