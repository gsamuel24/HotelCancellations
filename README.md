# HotelBookingCancellation-predictor  

### Authorship  
Grace Samuel  

---

## Project Overview  

### Research Question  
Can we predict hotel booking cancellations using customer and booking characteristics?

### Context  
Hotel booking cancellations negatively impact revenue forecasting and resource allocation. This project uses deep learning to identify bookings with a high risk of cancellation. While the dataset is from a simulated hotel environment, it serves as a stand-in for confidential work performed at Crossover Search Partners.

In a recruiting context, similar modeling can help forecast offer acceptance, candidate drop-off, or client engagement - empowering firms to proactively manage relationships and mitigate risk.

---

## Stakeholders  
- Hotel revenue teams
- Hotel management
- Housekeeping
- Head of Data Science (project lead and analyst)  

Model outputs include probability scores that can trigger targeted interventions—whether that’s preventing a cancellation or re-engaging a client.

---

## Hypothesis & Prediction  

**Hypothesis**  
Booking cancellations are predictable based on lead time, price sensitivity, guest history, and other booking details.  

**Prediction**  
Bookings with high lead times, prior cancellations, or certain market segments will show higher cancellation risk.

---

## Data Sources  
Simulated dataset with 35,000+ bookings, including variables such as:  
- Lead time  
- Guest demographics  
- Price per room  
- Special requests  
- Booking channel and room type  

---

## Data Preparation  
- One-hot encoded categorical variables (e.g., meal plan, room type)  
- Standardized numeric variables (e.g., lead time, price)  
- Extracted features from date fields (day of week, month, year)  
- Binary encoded target: `booking_status` (0 = Not Canceled, 1 = Canceled)

---

## Methods  

### Modeling Techniques  
**Model #1:**  
- 3-layer dense feedforward network  
- ReLU activations and Sigmoid output  
- Achieved test accuracy: 86.2%  

**Model #2 (Final Model):**  
- Deeper architecture with 5 layers  
- Dropout, Batch Normalization, L2 regularization  
- Improved generalization and calibration  
- AUC: 0.9352  

### Evaluation  
- ROC Curve and AUC  
- Calibration Curve  
- Learning Curves (training vs. validation loss)  
- Accuracy on holdout set  

---

## Tools Used  
- Python 3.12  
- PyTorch, scikit-learn, pandas, matplotlib  
- Jupyter Notebook + GitHub  

---

## How to Reproduce  

### Setup  
Install dependencies:  
```bash  
pip install -r requirements.txt


