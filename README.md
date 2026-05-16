# E-Commerce-Sales-Analysis
Developed an interactive Power BI dashboard integrating DAX calculations, KPIs, and multiple visualizations to provide comprehensive business insights into sales performance, profitability, targets, and regional analysis.

## 📌 Project Overview

This project demonstrates the use of **DAX calculations** and **interactive data visualizations** in Microsoft Power BI to analyze sales performance, profitability, targets, and regional trends.
The dashboard provides meaningful business insights through calculated columns, measures, and visual reports.

---

# 📂 Project Objectives

* Perform business analysis using DAX functions
* Create calculated columns and measures
* Build interactive dashboards and visualizations
* Analyze sales, profit, quantity, and targets
* Understand geographic and category-wise performance

---

# 🛠️ Tools & Technologies Used

* Microsoft Power BI
* DAX (Data Analysis Expressions)
* Data Visualization Techniques
* Business Intelligence Concepts

---

# 📊 Calculated Columns

## 1️⃣ Category Type

Combined the **Category** and **Sub-Category** columns into a single column for improved product classification and analysis.

### Example

```DAX
Category Type = Orders[Category] & " - " & Orders[Sub-Category]
```

---

## 2️⃣ Revenue per Order

Calculated total revenue generated for each order.

### Formula

```DAX
Revenue = Orders[Amount] * Orders[Quantity]
```

---

## 3️⃣ Sales Category

Categorized sales records as **Above Average** or **Below Average** based on sales amount.

### Formula

```DAX
Sales Category =
IF(
    Orders[Amount] > AVERAGE(Orders[Amount]),
    "Above Average",
    "Below Average"
)
```

---

# 📈 Calculated Measures

## 1️⃣ Total Order Count

Calculated the total number of orders placed.

```DAX
Order Count = COUNT(Orders[Order ID])
```

---

## 2️⃣ Average Profit in Delhi

Calculated the average profit for orders placed in Delhi.

```DAX
Avg Profit Delhi =
CALCULATE(
    AVERAGE(Orders[Profit]),
    Orders[City] = "Delhi"
)
```

---

## 3️⃣ Year-To-Date (YTD) Sales

Calculated cumulative sales over time.

```DAX
YTD Sales =
TOTALYTD(
    SUM(Orders[Amount]),
    Orders[Order Date]
)
```

---

# 📊 Dashboard Visualizations

## 📌 Sales Target Achievement by Category

Compared actual sales against target sales using a **Clustered Column Chart**.

![Image](https://images.openai.com/static-rsc-4/Myufr3DwELL3MkFENOXElgh5HFPo7d7VLW_Q9EnYfQpjaQueYRe275GkVXWolTq8eS_AfB1fD8nP7jRnczJoCLF1Jn8ZxIWB09DpkEDwKdUYIPX9ELKOxb1HH_cPAQUCMbqOw1iRqIAeQyDIA663t_EklYFUELDGNSIBR97g6rE6f4-GRAXzk0Kb94sgZGNd?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/DRsWviNIYZwOmHCZ4jm6W2O5rQ1p8_6o1HoT22YazcTsHJVgbJfKzqqfnMpQ30KY0hKkbWXPgIZAUbQIN6oV_n9G_vPNRJQXmK8IeuRdkuDsDB9b3b8rOqzFoNylmd4MrGYjVvmv6EXd4XomOvdM1kHbgS28HLmxq6TSSmJzoyHeL5hNXHVgX81Yk_N5KOlT?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/-LgvvI0hSp9ZBy1D_GZy4c_7wfishduQ3XgvISbdePBxHm4CtYUiUfZptOcAxfPk4jSWazbNQUW7l2dbgZzyXXGCN0n2XG7uSJxNAHnL5htbD98ixepVBgn4LBJqhqw5WkvebP670WtAdRHZqEkhKPfAnRlvtAa0q-gGUdTnfhLMZpSR55cFXe7gX9VaJ1p8?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/HNyNSKpEEK_YNQ1pUX8WZ3VJxIygIzf3aPKb7rGk3C04idWu5SC_V62UX3CezJTSTcjkYG5JLYZlEdPnNYG9ZCvv472HOs6ePLFEWmZjRQd2WXyTEuCM9eIalCTrUkH0UJ9a54zWwPKLIR4-HMgAZjemkD-87LUrg81ReF-h8eo3SmQiEBKZzeYJ9TqTGdsP?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/gaj3bCRwu0VBaSP-7ZNYVcqM9x21g6EByd-kFqL_yQxJtogbHtx-IgKZlQbA9N0q6WlNTIFueawBimsFEoqaRE3CgRfUaYjoLOTYzqki9qa_ORvez2uUrCjigV93DLvfHOPVr0sP46Lid_BEA7uRSSfUpL50BiFZyNGfNCMrPplAc0nBxPQXeKobsHr2ZzSe?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/PZhCfNcdmQUHXPWenNcYi7BmTrr7Vox15Egy3HGFIo72G6XuPYo8LU_5ElfaCsOjw8-PwET-bYrMJKExUN1W95v7Hq6Sp9lzAobsF6zGP-gMipJcHW8QJVgJIN35qeRA8XufZ_dbtBPVu9qefbtHKorg7OFt5iV4K8rCo8rAjxfkV5-KmU3UgiDfpH2d0hWC?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/tcPAcPsCOZh0RzwBJRJfvFfFi83oyY_965-miRNWYyzox_rWiybVzpVpwcJ2D1xJdOitJybwUIOoaPFoJQmCT5_-ghHzk-eaY3yvNVbCKrmWk8lZrUULCw4QFL6TMt1Td9wzwRutRiD4q8am1wPiWxkSPHW1wI_sfG653nirAxQ20lELJqUvcTW0Aw6fX795?purpose=fullsize)

### Insights

* Identified categories achieving sales targets
* Compared category-wise business performance

---

## 📌 Max Profit Margin by Sub-Category

Visualized maximum profit margins using a **Donut Chart**.

![Image](https://images.openai.com/static-rsc-4/Nnbp-Wr7JJrDUSSuv3bE7kXYdnRyh1EBupYJBSVlc-K14FcXogyZx1qguIVc3I0p_VfwM6oj4V1z7NNzObUAkZ3sH9KOrh1k3hNML700BZcrPXYXUkODPlT0G3Z2N6zOHrWYRcY8gbtqHSkMZEETj2Bx5VztUfkoQbPqPQ6Quf4ewupTOp9PGWBIvz-cX2w6?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Uof_6mDhg85pZn5wv9IHjkdmmgxnb2nbKt6UfXj2iZKnBnFTytF4sta2KTgLtASLexr247r1eyCFoJa6a7_QDIKQGQqNx_xluEL38GH24Ua7tVtGdBg2lWXusIznbR_iklvPkOPRs7xiQ2Pa0bGbvLBmTZVIqfllAuciBz8_BqAjza0scHxqwWa6nXucj2Aa?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/vx43vElvy_QmrA2GwTlIlcrEwzA3D_AXQ3OHTy_ZGVYb9qRcMia6PEyIwZIkhBdkV688StezOnpAtccxQGOD2LMLiTt93ZFRZnnPnVswhBVwHFi93IqgtT9A3gV_naVuGtWQ3POoICYFY2SPCtAtC6uUj13hXazg38VKVS3UUZREwbIT5gTETs1LMBD_jIL7?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/98-iYqBKUP_PsOIupNHWDo8KmvNj-MDX4OBcxPeYR5euPuN97FjFke2Yg6Lzr1K0wbstr5XWNNdTU6WsjWbXoqY9LFiJ7Zbntyl9bDsGbrriMhqSEQt0kpOQutzgYpq-0TR1M7jfzp2Rtr5prLz9nb1BRKpSD65aAXdMwCiTzCN-ZdxL4IrujUaAMeN440sQ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/ZKAohGgoknGq9SE8aJt2uMLjQj5uBNysPfuVCHyMnp8M0mxdwAAgoaSt6Tp9TSEkePMDij1R1n2tHKnighNZ1Kc1anXCoopXl1uskiM9yrUNvt95WuKf3mDmZtGNEYEE7xlbaUK0OTUNdZruQGk9ooIF6H73SWlP5Yrykj5iwBVixBAiB-6zFX9BYplEPmVN?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/czkV7C7CV1-Zv23WvxqH7pltXUEnLZ0I5BEWjubciZw8tJLhMDQRJGQQH-6zKUoaMXR8scsM__fXA7bdcPxdkW2hTCHkH-UUNnbnZyaX-hSAqBaSkgiZvJ_3zed0-1srB7iAir6XsJoACXtFtH4NIOqSdQaD7XAFuz8lXUQwFgbAPOexFJ73DHX4MqeVGrq4?purpose=fullsize)

### Insights

* Highlighted highly profitable sub-categories
* Identified low-margin products

---

## 📌 Monthly Sales Trend

Displayed monthly sales growth using a **Line Chart**.

![Image](https://images.openai.com/static-rsc-4/G04lD3BjZQgnKh73FAn5diNYE1nD6lXlvUz2yu9wXXh8DHA3YVMBDKLT_HTwMziL3Ci5FUMo2eamzo27BSEfqW74mD3wuOmAHgXLZjCjkdt1Myyqx6eLmppCrZ7m84C_WI1f5lv5XYLKNDg2oaJemrlvjLWrsP4HY8S19DDOb5aYe1sJtoazzg7OuvE5vw_H?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/UvClv1w4ChNskBwKhnOSlEz0LgXhyYQlHtQ__dVWbm0A69tb_TysE8OwPohFjxIEuVr6HiMQKW4BhsYn7I5SUX_gInvYUpRiF3lAbHcY09CZv8CLJgHQyfbt0Io9pyvtUzl1PkyuRhXMWWT90YGw0WUHYkKJ0UlLidU6vuZGxseqjVdAhCnvUvrbg1Hc_jFM?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/jAJgW8tUufNiL4O5L7Pkk7FSi1l-UEfQ5qk_Mf-wUBgi_zIiAOqzIvRoQJpNFsPgK4amRrfhRAN7zwy0NlaMOr4sgy3ui9d02DEtGfzNgRj88IQ0LEVcGlWl7EBp8UZzOTM4IWZNi4v_hu5cnBU0dZCHHJcRrLirHkR8bkPRjERTRy_og9v3oajEmfTlrd0M?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/9dTplh6vqa-2S-OTR8Pyqio_BVp-sgBvA-Az_YAhkg8beB4eNNiXtiQFST0BM5qlnHXBI9bG0xwpUsY3ExQ98w_CFcuUI78ZId_alS0KIvnj6ac3syK8p9aX7N6g_i6FxvRjMTxDwLFaRPdlOe5s5uAa3AX9h3yHhhCzwHxMKjSM1VD63OXGnP15hfQfegH4?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/XqgGqEpYjwftpa2xgtUSkGfOBQA4umX3H-fBJ8HrcLQZPA8twUuiXsjTr3C0Q0WSujhjvGLm_ozm9wCyP9x-_2kNDxRK85u-ZEKf1pXXu8resRrOyMDsuzvTBgGVkRSrk2u1JTOQ40mlljmbJ8OwWqRYIDXjnF9rmJHRR1hpvxTMxnsWaIzXGLJb9DCzV2Dp?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/RCdTzMO0UujFtZgs40zm3lfFmT5jYg2ChR2CHGboZYDIsm7sVI8IgRMtekRliXWOZg-Xc9RN8hLctN99he-x1UJh2ro8Lgsco4VJgsdyvXdJBp9fwRQsh2k9D1j4DlUzowVBSBm96f4ZbLiks1_FckozceWuNdsGq9-1v5WCRS_ZoaOVDpIs0RJ8FGnTuHsQ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/3PJWKuUvUajrMI1k5WVGuZwwXCSInQnJIe9dPxzEDhE47yGL4hdl-Q8yJVEr0Th2m0lUgOCWU9kr8GEYtTgFxBf2RBQFc9GzjlVyyoU2vL3gzMMTDABaZpO86RtzHteW6MPpcaYqofZGlriRIMoXEy0-DfgLGltTpdXrgQFuglhvFSAhreIjTCnL6zTlLcO8?purpose=fullsize)

### Insights

* Analyzed seasonal sales trends
* Identified peak sales periods

---

## 📌 Profit vs Quantity Analysis

Used a **Scatter Chart** to compare profit and quantity sold.

![Image](https://images.openai.com/static-rsc-4/RCdTzMO0UujFtZgs40zm3lfFmT5jYg2ChR2CHGboZYDIsm7sVI8IgRMtekRliXWOZg-Xc9RN8hLctN99he-x1UJh2ro8Lgsco4VJgsdyvXdJBp9fwRQsh2k9D1j4DlUzowVBSBm96f4ZbLiks1_FckozceWuNdsGq9-1v5WCRS_ZoaOVDpIs0RJ8FGnTuHsQ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/OyJiUTg7dz79hEUP21leTVJApi-yrzih2BGvqqfTWdW2-SlxzW_FW_rYLei6XY0W5ltG_H6Z-GTSBhllN2kaHfNm4MPQBw0JxZhb2hVuvvRDkYtQCjzZdQfh7ByquxV6nx2xA371vD8jR2vsrPv-kNN1ighUSWSZKnExY44dsoZJ1VtW4b2CyO8Ff7f0FngN?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/IrXoii_W4iQysgedj-9qNnZlGYp2WTORnxPZmRrnSTzJyrT4s4942ZmANSA2jb3rHrrDBGSYkulPeWQoJ1xMhZSFTXxc4Q55NAoplsWUJcqKaaK2G4Ed_OFzrZkDAO-Vbo0nQL81VByRJRanu8Kd7XhAm76CgKW83JP-X1YZ4jC-tNEzRwdW6KwEiZRlAtCT?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/N7PJE84i9V0y3c7vbzwt1wdldhK-XLieALAoH32nV_Bw3V55riQ2N6aW7TYGKjhCm1TJ3amJqGsuJ2-e-vucc2O9J9KwMW54fAEbHWYUB5WycbNAUnM-CTDhd036U5TDBdswt4zY5EzlqU-t-lV1M9cema38QBLrkCi1EplUvf1keDYH-CHaR5lxhCADdKHy?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/KJs5bCu84HggwnbWMMjCNU-7kUtVZFCkqwKCZ8ORG-CMCbQggqZTOMKC5qzXSfbQ7X9jqNqoXL7t1OiVwS3pQrclNEAkXK0v_N1c4gk_dsWs1lm8Wvb7rflXkxE6SZd4ziA4pY1FO_WYtqylATrNaGtv5KFihRh7xFuy-axlaUEfcZxjhWNiBAB_8isLyf-c?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/YLKKLWM3wMvJodoXrRumBccFbJ6OfFokL0sGY6QcLzXLCreDu5tFCeSDXaKRs7yqZ6x1QzWq_zux127GBG2WcOVlYq76hIR4zwuCwmIT4UsX2xt6V5Gy5UoHqKWPnGJhhNeGGQKZAyJZc2f3GxJlc54K6yB05lGk1Y9SseKBojGcYq7GIOPhiCxGB3ZK2Ope?purpose=fullsize)

### Insights

* Identified products with high sales but low profit
* Analyzed quantity-profit relationships

---

## 📌 Sales Amount vs Target

Used **Cards** and **Multi-Row Cards** to display KPIs.

![Image](https://images.openai.com/static-rsc-4/OBxUhHNYzxeikSSfutcBsEn_f1JUjQPldgZKrjO2lythCbgexF4430TrI7GRi_fFVw6gjJxfa-DidzYp2MpUGCvpNpkFZY6YpVm6PJbumke3moCGStqfvZ1Z2r9fuj07td7vHU1OyK2Z8x5G27d-Gy2GSczTNX7MI1ORyKyvVRC4DVVM6gAD9pYMXL-JasTO?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Kn_oSIyWEWIOGL27-RG77mt5vic6UpsGZp91zX0myZQGehMnxV1UA-7KmpwzaC8Yw6-vZ-2SCBTgiIbBF3zs8cYF-aPZueU6yWAI9SkJypYF02InFz8XXbvU-nBwXvWjW5a8VJy8Y1-VNvN4YUs5fkLyLkA5waLijH6QQf6_IeUa5-Agr4CiMiRGeK5nKm_9?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/21zsb397OfTSMDJbCGOEKgLIASMkGyD-1MOVGa9P7gR1JkjowlrCi3Aqf1Wve6WNxfSaOGZLWDlaNDFGSLaN-3eujgV-cJedgwqga0y2-MhnqJvAXpR37qLaKV3FYnV-oa6phMehctkVuuATlpH4uPRfhDcfxxmUEgBLgDfvnOgwLl7Wt3QYIoc9aauaBOTK?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/hnGpIZbmOzLpu9HarHwkIPyvCoeyrOcL1VG2DZziVesIHapZAN5f16e6hfNiWTq2a4HILBJ_OmFn5OumQ_B4GHHsCLIyBlX-3U2VFD6wniARjz-PmiEORdzExRh1RAt-MoWSNtpGbDkB4wUgO_F3lnyqxaGrRwvERH37CKX2YbzmosbWcCOqlGtWbcZxjFfv?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/rnLydCjP8zROu3hEp7qWT14WK-PmIB20P1iO9K-DMo-yx5BmTL5xoP-8AT8MZTqP9dm79nRzWXSuevWPing-atzWjjBx4Gqzk-oZbGy0whTwDa4uXgq1wyWn_hPVMPRb1-pRe2hh96uNm8tNSySPGvDriZ7GeNn-j4CyJU5lrYYp_dW90FeqwRwUSMWzQmWw?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/feFm_MV675QM8wAEvcrpP53KZYcgzmlOQTrQcj4OxOVkquEdLNSg2rMXUJom86yGm00HCx0hXRf66cUFD3sqSiay3LCmA7gqFygbBK8H-TOxB0SmzowwyNH91OGkSEuqNn-jDI1H7vv3c1KFQFDrGR97w24hkHx1dLchN3DcAT1smrahw6zDrQukb84f04RC?purpose=fullsize)

### Insights

* Quick comparison of actual sales and targets
* Segment-wise minimum target analysis

---

## 📌 Sales Performance Matrix

Created a **Matrix Visualization** for category and monthly comparisons.

![Image](https://images.openai.com/static-rsc-4/Ot4oPb_vMo50-WxcKOKrYTP-doQv09beQsWNixK3lSJ5YbsElQj7H3jsqmxQusata--HJiH_FfPOSA2jygw0iRaa_d6tz1krU8QpK9VKo_6NVbEF2PueR-peiWHygHP8cozj3mK0JfaJjCSEV_zNr8EgFVIOq4XS1tKaddSf_g3BQYJGsbnAPHfXdivlkBzR?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/3tkZttZhQEOpgDHI-X5SreXm12AXJqeIkl8x7KyfKz4fkQ950YNO6xa4oWQdUW_fxhCkQ7nGquMEp6HTXBxv_ET8A9bEv2ncSKmqQCWqYeAfgmFt7uN2aOM-Z5UyuduCB8pVavC0KYU_ZH49uvdjVjfQKsklPGef-4OwHENln_7B41ZwzEfhyWmWT8xsTn59?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/9TGZo7HWTvST85os7fC4stJihd4l0yT5e1IpgHVpQW8YJw1_rgmcSctgSVvC84QQHZ9pGbm67Q9aJlOE1e6lXA-wm1a8CsQORAiNVVByJYFdrG1p_zcX5vXOo1KgQ5c3-XrHw62HcdrTIguMTgKdiSu7sl4tc0t3B79Syakau912UNfBq9msbSrRlrOm-Qkn?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/9dTplh6vqa-2S-OTR8Pyqio_BVp-sgBvA-Az_YAhkg8beB4eNNiXtiQFST0BM5qlnHXBI9bG0xwpUsY3ExQ98w_CFcuUI78ZId_alS0KIvnj6ac3syK8p9aX7N6g_i6FxvRjMTxDwLFaRPdlOe5s5uAa3AX9h3yHhhCzwHxMKjSM1VD63OXGnP15hfQfegH4?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/1ikwvKRA_9j5EiAsApUg7akOkQjZgVV9-34lGgaTxHAldpuq8kJMZcSrvia5kf44o66f3M_Ui5xCNxR-QdCaD1CVKP7ZNs6gU1wn5SG9wn-mgFvgTazsKp2TMYe9dOyONVokun96JFlMcr9tlMNIi0A11_mKTHYm5bjXpjVVM5OXSyVOmqmiSMO_J0pAvDF0?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6Uz3pEoM7OOl1XZY6cSneSb_2vRQQzktGE1AbPJzweAmzGFeO76j3aEXfz1gR6P4CfeuUFCTGtZFUCrXSvqb8f7ITJPDygfCLF2GSRI7WLhQie3HFEkh3AGRWhRlIkAJ6eY8jgYECyqIsFdOdRj6OiDp8rYnxrhT06G57xKjn6VQCrsqEE9BqCF0YLf0C_uN?purpose=fullsize)

### Insights

* Compared monthly category performance
* Evaluated sales target achievement

---

## 📌 Geographic Sales Analysis

Visualized city-wise sales using a **Map Chart**.

![Image](https://images.openai.com/static-rsc-4/TzQmQ9zBUTFcDR3BwglMCXugFY22a7cSZIkCBSRJEL3J6ZFlKHqa5iDpirF-0u54vVu7TZ6JrVj_imQ8Vmc7bPKn0agrjL1yYy1vWQ_dsAJnpVLZNhbuojYDlvgMG0fNvPtlqszEYMOJ4aZReUul2qyrsQmjR_kX1TI6roAghRB2bkp3DfHvLqAD3ixJ_vX6?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/6Wwfm5lpPIFdz8UggskUxVlfIRhDVRO4sXHFkFFLkmOspOxYbvvDy8QXy3cJgL371ugb0TMtDHzLgwe3Ja0VdZzRtn8asyTHMRwIHsM17KtNI5LvFDm7RJugjIKuE2VHcsVcRKDS9kUR3P0_qbbxJWk1S7Aj7upwd4XZctiHBavcb_2G29hZuGgVSmNEjTTu?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/tcPAcPsCOZh0RzwBJRJfvFfFi83oyY_965-miRNWYyzox_rWiybVzpVpwcJ2D1xJdOitJybwUIOoaPFoJQmCT5_-ghHzk-eaY3yvNVbCKrmWk8lZrUULCw4QFL6TMt1Td9wzwRutRiD4q8am1wPiWxkSPHW1wI_sfG653nirAxQ20lELJqUvcTW0Aw6fX795?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/9dTplh6vqa-2S-OTR8Pyqio_BVp-sgBvA-Az_YAhkg8beB4eNNiXtiQFST0BM5qlnHXBI9bG0xwpUsY3ExQ98w_CFcuUI78ZId_alS0KIvnj6ac3syK8p9aX7N6g_i6FxvRjMTxDwLFaRPdlOe5s5uAa3AX9h3yHhhCzwHxMKjSM1VD63OXGnP15hfQfegH4?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/vDrOm_a6VxPu03Qc_T9DMC67NKEQoDhwfUHHZQS3-88h6ohe634W2K5qM5NE_yEHWJ5Q3MMa0iI5q8Q0cea8hr0Fe1DuwG3QQkSea5IhIYJvYTM3YcdudLMVv5_hYSu6dALZEMVaHjFGadTud8-ySbzte2ofTZtf01OQPuGgM2iffeASlF990zszAe8X0264?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/DRsWviNIYZwOmHCZ4jm6W2O5rQ1p8_6o1HoT22YazcTsHJVgbJfKzqqfnMpQ30KY0hKkbWXPgIZAUbQIN6oV_n9G_vPNRJQXmK8IeuRdkuDsDB9b3b8rOqzFoNylmd4MrGYjVvmv6EXd4XomOvdM1kHbgS28HLmxq6TSSmJzoyHeL5hNXHVgX81Yk_N5KOlT?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/DAgKMaR0ujvCiFxkSsGWnumOPWqsFTdVT8cnkaGDq6AjQ-wOlId6GuiLhE-89CJOOxnDi6EaN2SpDnlaYSEm2eJSe4lk9hdTWQ3a1MqiUjlSw7Cb4e7FZ41XOYHs3yPdzF0nb6Yx0f1kjvNVAorYVBl8M7oRzf80uVcgd8z81zY44DkvzaXN9450ca1dwyH9?purpose=fullsize)

### Insights

* Identified high-performing cities
* Analyzed regional sales distribution

---

## 📌 Sales Distribution by Sub-Category

Represented sub-category sales contribution using a **Treemap**.

![Image](https://images.openai.com/static-rsc-4/VaIN3DhWlEker0seW-DfhuXA3PvhM2rIoedIsxtG4z9rAk4ZucarT1c7XTBRoNCUEpGdyk-i0Jg1gk7h3FYa0q0NzYkar6aDSpeAzgUpHzqIQ2SXrPn7wy0OBkf4kZFvM_hdUWHxSVu4gR2yfNjZfmQOa28Tqc4ci-8bTgEkljwfBZv4GsUxl6LYJSR2NoDJ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/uUgsem82roEN5vIg-s-8ndnSq8DANh681VANLoDV6XIByj-b_x8I_Z-5gYAWCAWdGJEKK8k3yPPW-eh_fU2jJ-LvVrgC6DA-YVD_x4poxnl_st2fxAmqTYUxqSFLx3YAcYxue7ChYOL4eaaSJFBDgJkcejHItVaOveyjL5nQhf9nj6HzMFBXArMzgM_24gnZ?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/4HGYwJotDHTEIqy4TH3LKP6w199blGL5ALTPv3-98FUc1GOuUefC1eV3r9I6nutL57DeJekPoUD5fmfq2cHH7E7NpntY9fpg57w-_YQApHlYIPkHWNJ8erxo65B2yGuRT5c3zYO1TJ51Xwd0lznp7xxaCoCe0TwTM3zFHMLCnlmC6OZzYgxyigAaj3rRAaGd?purpose=fullsize)

### Insights

* Identified dominant sub-categories
* Visualized proportional sales contribution

---

## 📌 Order Count Analysis by State

Created a **Funnel Chart** to analyze order distribution across states.

![Image](https://images.openai.com/static-rsc-4/g3_jv7Eqy4Hwdvp9PWinRXwpJdtFPG2YOIdiX8scjteyZosUu15XR-_Gfm4rtMg5docXAn9JGfEUzVR8gX4kzuvn5pF6pHphATSGGxFWnSEp7WK79HSX1qo2wscWYkdIxTDAc18jFVdDjkDWBr1UpxHdOWVCyQMPkFLlozlq2LyvpJkgrXyp-JIF6PN8CS8l?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/wU_8kGXzhePI4NnE6TqLrYS_HX7xEcJ5hQhnWcXVXWwvvKJTE8eu8raTE6L15tPUC5y-NOoENqU-z59PEAY5yqkmRIVFsopf17vLgeMgjzK123W6xvV-zPkhd-0H1dRJL0m3fi4z-BpdDat7VdSEAa8IUVfUYP3xk0JSaNhURKm8j6uSJGbuZAsZZzhL4Nup?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/HNyNSKpEEK_YNQ1pUX8WZ3VJxIygIzf3aPKb7rGk3C04idWu5SC_V62UX3CezJTSTcjkYG5JLYZlEdPnNYG9ZCvv472HOs6ePLFEWmZjRQd2WXyTEuCM9eIalCTrUkH0UJ9a54zWwPKLIR4-HMgAZjemkD-87LUrg81ReF-h8eo3SmQiEBKZzeYJ9TqTGdsP?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/oCnmZ3Jui5WGErWgBMG_PvV-A6PsN8IW_k90qELNXGRhRggNvIE7CPOoTZ3DQeZByiZlNKzOR4HZTQ4uog_BjDalfIieFHgF4cKj_xRXHBluO3K3T8DiuSbTrWe2oNYf3_dS2bv-jEpiVgcJNZMobwGPqsFHEb5BxAgcJ0hQvLwOLpygivetm6RPhi0VT6Z6?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/cWUFFvYLcnrmvEWiH79q5Xs1P-G6IbOVlJ1u7b2s27v9zsNBUaFyQTl20LMKqBrvCx98iLX08whd0Jbb-I6eAxnqwoZFKNqJ_Z3VAXvzIaos9odA5klcfrkBgdCrXZWN5Ys6UOX22wpa2JYNjb-2CxpxA_fqsHExv97iqK-i8yAjHsyVptx9JoBCm0OnTe5s?purpose=fullsize)

![Image](https://images.openai.com/static-rsc-4/Ga2FiE5CWZq6hNLTjzEr9PYXJm0X2AfTsajFWqR7yO-qkluQ5AJOmKpGuMlNm8FhjaVuvjHZlpv07YIw4mRanDwgmpzkmKLuH1LNS908ePE_GlBXDPAvTY7Mr2IsJi0gMHY7_d5Un6Eyc308kGxM1iuffZGFAuKfl8wMh_crVWDWrb_LpwCLFo88X-5dzNXT?purpose=fullsize)

### Insights

* Compared order volume across states
* Identified top-performing states

---

The final dashboard integrates:

* DAX calculations
* KPI cards
* Interactive charts
* Geographic analysis
* Sales target tracking
* Business performance insights

---

# 📖 Key Learnings

* Understanding DAX formulas and calculations
* Building interactive business dashboards
* Data storytelling through visualization
* KPI and sales performance analysis
* Business intelligence reporting

---

# 🚀 Future Enhancements

* Add forecasting models
* Integrate real-time data
* Create drill-through reports
* Implement advanced filtering and slicers

---

# 📌 Conclusion

This project successfully demonstrates the application of **DAX calculations** and **Power BI visualizations** to analyze sales performance, targets, profitability, and regional trends.
The dashboard provides meaningful business insights that support data-driven decision-making.


to showcase the complete project professionally on [GitHub](https://github.com?utm_source=chatgpt.com)
