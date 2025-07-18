# Data-Visualization-Phishing-Detection-Datasets
This repository contains data visualization results of phishing URL characteristics using Power BI. The goal of this project is to explore common features in phishing URLs and compare them with non-phishing URLs through informative visual displays.

Phishing is a digital fraud method that often utilizes malicious URLs to steal personal information. Using a dataset of labeled URLs, this project visualizes various characteristics that can be used to identify patterns in phishing URLs.

**Tools Used**

1. Open-source dataset from Kaggle
2. Jupyter Notebook (for preprocessing)
3. Power BI Desktop (.pbix)
4. Dataset Source The dataset can be accessed through Kaggle:
  
   https://www.kaggle.com/datasets/simaanjali/phising-detection-dataset/data

**General Insight from the Visualization Results**

Based on the overall visualization of phishing and non-phishing URLs, both with and without the use of slicers, several key conclusions can be drawn that highlight common characteristics and suspicious patterns found in phishing URLs.

**General Distribution of Phishing URLs**

Phishing URLs make up 15.87% of the total 630,070 records, representing a significant security threat. These URLs often attempt to mimic the appearance of legitimate URLs — in terms of length, use of symbols, and directory structure — to avoid detection.

**1. Impact of Number of Dashes (NumDash)**

Phishing URLs are most frequently found in categories with a low number of dashes. This indicates that attackers intentionally design URLs to appear normal and trustworthy, reducing the chances of being flagged by detection systems.

**2. URL Length**

While most phishing URLs fall within the short and medium length categories, there is a noticeable trend where the proportion of phishing increases for very long or extremely long URLs. This suggests that attackers may exploit longer URLs to obfuscate malicious content or insert fake parameters.

**3. Path Depth (PathLevel)**

Phishing URLs tend to have shallow or medium path depths. A simpler directory structure is likely used to disguise phishing attempts and make the URL look less suspicious.

**Effect of Combining IpAddress and HttpsInHostName**

Among domain-based URLs that contain the word “https” in the hostname, the phishing proportion is alarmingly high (76.6%). This implies that attackers may insert “https” in the hostname as a deceptive tactic to create a false sense of security.
In contrast, domain-based URLs without “https” in the hostname show a much lower phishing proportion (14.81%), indicating that this manipulation is a distinct characteristic of certain phishing patterns.
For IP-based URLs, more than 85% are classified as phishing — regardless of whether the hostname includes “https” or not. This strengthens the insight that IP-based URLs are a strong indicator of phishing, especially when combined with other suspicious elements.
In highly suspicious categories within the HttpsInHostName variable, 100% of the data points are identified as phishing — despite the smaller data volume — suggesting that text pattern detection within hostnames can be highly effective if further developed.
Consistent Patterns in Slicing

Across all combinations of slicing (between IpAddress and HttpsInHostName), phishing patterns consistently appear in URLs with low NumDash, short to long UrlLength, and shallow to medium PathLevel. This consistency suggests that technical characteristics of phishing URLs remain relevant even when analyzing data subsets, supporting the idea of using multi-feature approaches for phishing detection systems.

**Conclusion**

This visualization highlights that while not all URLs with suspicious characteristics are phishing, certain patterns — such as the use of IP addresses, the insertion of “https” within the hostname, unusual URL lengths, and simplified path structures — can serve as early indicators. Combining these features, especially through interactive filtering and multi-dimensional analysis (as done in Power BI), provides strong support for building rule-based detection frameworks or as a basis for machine learning approaches in phishing detection.
