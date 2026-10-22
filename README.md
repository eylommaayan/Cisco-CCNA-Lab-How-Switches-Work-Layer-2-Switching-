# Cisco CCNA Lab: How Switches Work (Layer 2 Switching) 🔄

## 📝 אודות המעבדה (Lab Objective)
מעבדה זו בוצעה ב-Cisco Packet Tracer ומטרתה להמחיש את מנגנוני הליבה של מתגי תקשורת בשכבה 2 (Data Link Layer). 
במעבדה זו חקרתי וניתחתי בזמן אמת (Simulation Mode) כיצד מתגים לומדים כתובות MAC, כיצד הם מקבלים החלטות העברה (Forwarding), ומה קורה כאשר יעד התעבורה אינו ידוע למתג (Flooding).
<img width="1712" height="871" alt="image" src="https://github.com/user-attachments/assets/ad68e014-c984-43c0-b808-7a129389813d" />
## 🏗️ טופולוגיית הרשת (Topology)
הרשת מורכבת מתת-רשת יחידה (`192.168.0.0/24`) וכוללת:
* **2 מתגים (Switches):** מחוברים ביניהם דרך ממשק `Fa0/3`.
* **4 מחשבי קצה (PCs):**
  * `PC1` (192.168.0.1) מחובר ל-Switch1 ב-`Fa0/1`.
  * `PC2` (192.168.0.2) מחובר ל-Switch1 ב-`Fa0/2`.
  * `PC3` (192.168.0.3) מחובר ל-Switch2 ב-`Fa0/1`.
  * `PC4` (192.168.0.4) מחובר ל-Switch2 ב-`Fa0/2`.

---

## 🛠️ מהלך הניסוי והפקודות (Lab Execution)

### 1. מצב התחלתי
המעבדה התחילה כאשר טבלאות ה-MAC של שני המתגים היו **ריקות לחלוטין** מכתובות דינמיות.



### 2. יצירת תעבורה (Ping) ב-Simulation Mode
מתוך המחשב המקור (`PC1`), הפעלתי את שורת הפקודה ושלחתי הודעת ICMP Echo Request (פינג) אל `PC4`:

<img width="1707" height="877" alt="image" src="https://github.com/user-attachments/assets/8a68430f-6c71-4718-9b3f-d93fa6e2445d" />

