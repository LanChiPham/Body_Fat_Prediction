# Body Fat Prediction

Source: https://www.kaggle.com/fedesoriano/body-fat-prediction-dataset

## Attribute Information:
1. Density determined from underwater weighing
2. Percent body fat from Siri's (1956) equation
3. Age (years)
4. Weight (lbs)
5. Height (inches)
6. Neck circumference (cm)
7. Chest circumference (cm)
8. Abdomen 2 circumference (cm)
9. Hip circumference (cm)
10. Thigh circumference (cm)
11. Knee circumference (cm)
12. Ankle circumference (cm)
13. Biceps (extended) circumference (cm)
14. Forearm circumference (cm)
15. Wrist circumference (cm)

## Task Details
1. If you have some experience with R or Python and machine learning basics, this is the perfect task for data science students who have completed an online course in machine learning and are looking to expand their skill set before trying a featured competition.
2. Prediction for the body fat percentage for a test set. Note that the use of the Density variable is not allowed since the body fat is calculated directly with the density.
3. Evaluation: Evaluation using RMSE


## More details:
A variety of popular health books suggest that the readers assess their health, at least in part, by estimating their percentage of body fat. In Bailey (1994), for instance, the reader can estimate body fat from tables using their age and various skin-fold measurements obtained by using a caliper. Other texts give predictive equations for body fat using body circumference measurements (e.g. abdominal circumference) and/or skin-fold measurements. See, for instance, Behnke and Wilmore (1974), pp. 66-67; Wilmore (1976), p. 247; or Katch and McArdle (1977), pp. 120-132).

The percentage of body fat for an individual can be estimated once body density has been determined. Folks (e.g. Siri (1956)) assume that the body consists
of two components - lean body tissue and fat tissue. Letting:

* D = Body Density (gm/cm^3)
* A = proportion of lean body tissue
* B = proportion of fat tissue (A+B=1)
* a = density of lean body tissue (gm/cm^3)
* b = density of fat tissue (gm/cm^3)
we have:

D = 1/[(A/a) + (B/b)]

solving for B we find:

B = (1/D)*[ab/(a-b)] - [b/(a-b)].

Using the estimates a=1.10 gm/cm^3 and b=0.90 gm/cm^3 (see Katch and McArdle (1977), p. 111 or Wilmore (1976), p. 123) we come up with "Siri's equation":

Percentage of Body Fat (i.e. 100*B) = 495/D - 450.

Volume, and hence body density, can be accurately measured a variety of ways. The technique of underwater weighing "computes body volume as the difference between body weight measured in air and weight measured during water submersion. In other words, body volume is equal to the loss of weight in
water with the appropriate temperature correction for the water's density" (Katch and McArdle (1977), p. 113). Using this technique,

Body Density = WA/[(WA-WW)/c.f. - LV]

where:

* WA = Weight in air (kg)
* WW = Weight in water (kg)
* c.f. = Water correction factor (=1 at 39.2 deg F as one-gram of water occupies exactly one cm^3 at this temperature, =.997 at 76-78 deg F)
* LV = Residual Lung Volume (liters)
(Katch and McArdle (1977), p. 115). Other methods of determining body volume are given in Behnke and Wilmore (1974), p. 22 ff.

