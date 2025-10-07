# 🏨 Hotel Reservation Performance Testing using Apache JMeter

## 📖 Project Overview
This project evaluates the performance of a demo hotel reservation system using **Apache JMeter**.  
It simulates multiple users logging in, searching for hotels, and completing bookings to measure response times, throughput, and error rates.

---

## ⚙️ Tools & Technologies
- **Apache JMeter 5.6+**
- **Java JDK 8+**
- **GitHub**
- **(Optional)** Postman for API validation

---

## 🧩 Test Scenarios
| Test ID | Scenario | Request Type | Description |
|----------|-----------|---------------|--------------|
| T1 | Homepage Load | GET | Open the main page |
| T2 | Login | POST | Submit login form |
| T3 | Search Hotels | POST | Enter search criteria |
| T4 | Book Hotel | POST | Send booking details |
| T5 | Logout | GET | Log out from system |

---

## 🚀 How to Run
1. Open **Apache JMeter**.
2. Load the test plan:  
   `File → Open → Hotel_Reservation_Test.jmx`
3. Set Thread Group:
   - Threads (Users): `10`
   - Ramp-up Period: `5`
   - Loop Count: `2`
4. Run ▶️
5. Observe results under:
   - **Summary Report**
   - **Aggregate Report**
   - **Graph Results**

---

## 📈 Example Results
| Test | Users | Avg Response (ms) | Error % | Throughput (req/sec) |
|------|--------|------------------|----------|----------------------|
| Login | 10 | 800 | 0 | 5.2 |
| Search Hotels | 10 | 1100 | 0 | 4.7 |
| Book Hotel | 10 | 1300 | 0 | 4.5 |

---

## 📊 Generate HTML Report
After test:
```bash
jmeter -g results/results.jtl -o results/report
