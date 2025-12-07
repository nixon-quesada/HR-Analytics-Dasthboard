# Emerson-x-DAPH-National-Data-Challenge-Manufacturing-Dashboard

![image](https://github.com/user-attachments/assets/046c6208-85f1-4e01-b0b6-d517fb30386c)


### 📁 Project Structure

```text
Loan-Approval-Machine-Learning-Project-Learning-Classification-using-XGBoost-and-SHAP/
│
├── README.md
│
├── assets/
│   ├── backgrounds
│   ├── icons
│   └── inspirations
│
├── data/
│   ├── Manufacturing Line Productivity.xlsx
│
├── output/
│   ├── dashboard
│   ├── data analysis
│   └── screenshot
```

### Project Background
Developed as part of the Emerson x Data Analytics Philippines Challenge, this project features a dynamic and insightful dashboard built from real-world manufacturing line data.

The primary objective was to design a production-ready analytics dashboard that not only surfaces critical operational insights but also serves as a testament to our data analytics expertise—from data wrangling and visualization to actionable interpretation tailored for industrial decision-making.

![image](https://github.com/user-attachments/assets/e365fd61-8536-4c00-aabf-3bd0ff0885c6)

### Data Structure & Initial Checks

Manufacturing Line Productivity dataset structure as seen below is an excel workbook consists of 4 sheets: Line Production, Products, Downtime Factors and Line Downtime with a total of row count of 117 records.

![image](https://github.com/user-attachments/assets/81a24ee4-6f99-45c1-b8dd-611c44573e27)


### Executive Summary

![image](https://github.com/user-attachments/assets/78cf5dc2-56f9-460a-8b9e-37130a5a85d9)

Overview of Findings:
The production line is experiencing significant performance challenges, primarily driven by unplanned downtimes, which account for a substantial 56% of the total operating time. Over half of these downtimes are attributed to machine failures and inventory shortages often requiring frequent machine adjustments and additionally prolonged batch changeovers both contributed to 36% of the total downtime, further compounding the issue. 
As a result, the team is frequently required to work overtime to meet scheduled production targets, highlighting the urgent need for operational improvements.

### Insights Deep Dive

Over the 4-day production period, total downtime exceeded 50% of the total operational time, with the majority attributed to recurring machine failures and inventory shortages, along with several minor unplanned interruptions. Notably, 74 minutes of downtime were recorded under the “Others” category, indicating unclassified or untracked issues that may require further investigation.

![image](https://github.com/user-attachments/assets/1550a56b-4c25-419f-97c5-e3a85112dded)

In addition to an unusually long planned downtime due to batch changes on August 29, and the unclassified 74 minutes of downtime, the most critical concern is the series of random machine failures observed between batch processes on August 30. Even more concerning is the recurrence of failures after machine adjustments on September 2, which strongly suggests that the equipment may be approaching end-of-life or in need of replacement.

Furthermore, the persistent inventory shortages point to potential inefficiencies or disruptions in the supply chain, as materials consistently fall short of production requirements. These issues collectively highlight an urgent need for equipment reliability improvements and supply chain optimization.

The primary contributors to total downtime are Machine Adjustments, Batch Changes, Machine Failures, and Inventory Shortages. Notably, two of these—Machine Adjustments and Batch Changes—are currently categorized under Operator Error, despite being planned downtimes related to routine maintenance and operator shift transitions. This classification unfairly skews operator performance metrics and should be re-evaluated, as it may inaccurately reflect on operator efficiency.

Additionally, Labeling Errors should be classified as Operator Error, given that they directly result from improper label switching, a task within the operator's responsibility. Clear categorization will ensure more accurate performance assessments and help target the appropriate areas for process improvement.

![image](https://github.com/user-attachments/assets/3c26ae40-61bb-441a-9a4b-dce772b6ca30)

While product type is not a direct cause of downtimes, it indirectly reflects inefficiencies or disruptions within the supply chain. The leading contributor to downtime—Machine Adjustments—is often a consequence of recurring machine failures, reinforcing the need to prioritize equipment reliability and maintenance strategies.

Moreover, Batch Changes, which rank as the second highest contributor to total downtime, frequently occur in conjunction with inventory shortages and machine failures, suggesting that these issues are interrelated. This further emphasizes that the two most critical areas requiring immediate attention are machine failures and supply chain disruptions, as they trigger a cascading effect on multiple downtime categories.

# Recommendations:

![image](https://github.com/user-attachments/assets/b03b36c7-16ef-4c09-897a-a40472b715b0)

### Assumptions and Caveats:

Throughout the analysis, multiple assumptions were made to manage challenges with the data. These assumptions and caveats are noted below:
- The batch runtimes is effectively the sum of minimum batch time and downtime. However, this creates challenges when applying standard Key Performance Indicator (KPI) formulas. The minimum batch time represents the ideal time required to produce a batch without any interruptions, it is assumed min batch time are runs without errors and not the ideal time. To avoid misinterpretation, especially since many KPI formulas rely heavily on the concept of ideal time, I deliberately avoided using KPI metrics in this analysis to maintain clarity and accuracy.
  
- Daily production start times are inconsistent, with no fixed interval observed. As the dataset provides no explanation for this variability, it was ignored from the analysis.
There is a one-day data gap (Sunday), and September 3 only reflects overtime work carried over from September 2. Additionally, the data is not continuous, with production running only 8 to 10 hours per day over a total span of approximately 2.6 actual production days. Due to this limited and irregular data coverage, hourly breakdowns and the use of slicers were avoided, as they would offer little analytical value and may lead to misinterpretation.

- The dataset did not specify which downtimes were planned or unplanned. For the purpose of analysis, I assumed that Machine Adjustments (maintenance), Batch Changes, and Label Switches—as part of regular production routines—are planned downtimes. All other downtime events were classified as unplanned.

- The criteria for scheduling specific products for production were not specified in the dataset. It is assumed that production scheduling is driven by demand, although no explicit data was available to confirm this.

### Design
![image](https://github.com/user-attachments/assets/8a964fae-5bd9-4629-aa37-128e76e05707)

- A uniform 10 pt padding was applied around each container, along with a 10 pt internal margin within each graph and visual. This ensures consistent spacing, allowing each element room to "breathe" without clutter. The layout creates a clean, organized appearance, offering a subtle illusion of spaciousness while maintaining a compact and accessible visual structure, with all key visuals comfortably within the viewer’s eye range.

- All design layers have been systematically organized to support future collaboration and seamless handovers. This structure ensures that other designers can easily navigate, modify, or build upon the project, facilitating efficient updates and design changes.

- The dashboard follows a modern minimalist design, utilizing a glassmorphism-inspired UI to achieve a sleek and elegant finish. To maintain a clean and uncluttered interface, supporting details are tucked into info buttons, allowing users to access additional information on demand. The dashboard is designed to be visually adaptive, blending seamlessly with various wallpapers and background themes for a cohesive and refined user experience.

![image](https://github.com/user-attachments/assets/671d799e-e661-4eea-a025-7267a996bb3b)





