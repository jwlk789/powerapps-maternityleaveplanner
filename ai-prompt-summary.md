# AI Prompt Summary

This AI prompt was used to co-develop a Power Apps tool that calculates and visualizes a maternity leave plan based on:

- Start date of remote work
- Paid leave entitlements (child care, maternity)
- Optional PTO and unpaid leave
- Official company holidays (which extend paid leave)
- FMLA eligibility and concurrent tracking

## Core Logic Highlights

- **Holidays:** If a holiday falls during a paid leave block, it extends that block (such as a holiday during Paid Child Care Leave adds an extra paid day).
- **Conditional Leave Types:** Based on user toggles, the app can include/exclude PTO and unpaid days.
- **Leave Buckets:** Once a category (e.g., Paid Maternity Leave) is filled with its eligible days, the app continues to the next type (such as PTO).
- **Transition Plan:** Remaining working days after protected leave ends are marked as a Transition Plan.
- **FMLA Tracking:** Paid and unpaid leave types count toward FMLA, but Transition Plan days do **not**.

## Display Notes

- A summary list is generated showing each leave day in the format:  
  `Monday 09/01/2025 – Paid Maternity Leave | Pay Period: B091 (08/25/2025 - 09/07/2025) | FMLA: yes`
- Transition Plan days are excluded from the summary via conditional logic.
