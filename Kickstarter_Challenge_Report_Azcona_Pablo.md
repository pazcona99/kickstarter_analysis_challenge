# Kickstarting with Excel

This is a report provided for the Berkeley Data Bootcamp Module 1 (Excel) Challenge 1.

## Overview of Project

Louise not only has a passion for the artistic crafts, but also the data behind them. Louise was provided a host file containing a tabular data set of a campaign and their associated production. Each campaign had variety of attributes tied to them including, but not limited to, monetary goals and pledges, launch dates, deadlines, categories, and subcategories. Louise had her own play for which she tracked its fundraising goal successfully; however, she also wanted to know how other campaigns performed relative to their own launch dates and monetary goals. From this dataset, there is a visually apparent story that comes from combing through and analyzing the data. 

---

## Purpose

Not every campaign is **suceessful**, and not every campaign reached it's **goal**. Theses statements are not that simple, and the data can be used to provide a deeper analysis of what makes one campaign more succesful than another. There are certain trends that will be observed within this report. For the purpose of this report, an analysis will serve as a visualization of the data from two perspectives. The data will be reformatted to better understand the outcomes of a campaign `based on their monetary goals`, and the outcomes of a campaign `based on their launch date`. This help provide clarity to the original purpose of what made one campaign more successful than another and vice versa. For example, did having a higher goal have a positive correlation with more successful campaigns? Or did having a launch date of the campaign during a certain month yield better results? These are limited questions to which the analysis will help shed better light to. 

---

## Analysis and Challenges

### Analysis of Outcomes Based on Launch Date

For this analysis, from each campaign, the year that it launch was extracted from the dataset. From this, a pivot table was seamlessly made such that it illustrates the number of outcomes (i.e. successful, failed, or cancelled) to a particlar month of the launch date. This table was made so that it could be further refined to filter by the year and the parent category of the campaign. For the puposes of this analysis, only *theater* campaigns, for all years, were observed within this subset of the dataset. 

Interestingly, the overall trend, when not filtering for theater campaigns, inidicated a higher success rate between the months of May and June. There were sharp declines in the success rate after June and between November and December. Conversely, the failed rate stayed consistent overall with a slight upward trajectory between April and July. The overall trend suggests that many campaigns peak during the late spring and early summer months.

The line chart provided below illustrates the number of successful, failed, or cancelled theater outcomes in relation to the month of launch on the x-axis. Moreoever, when filtering for the theater campaigns only, a `visible peak is observed in the month of May` followed by a sharp decline for the rest of the year. The `failed outcomes of the theater campaigns is maintained at approxitmately 40` throughout the year. The number of cancelled theater campaigns is maintained below 7 throughout the year.  

![Outcomes vs. Launch Date](Resources\Theater_Outcomes_vs_Launch.png)

The challenge associated with this particular activity is derived mostly in the ability to add contents to the right fields. This comes with an understanding of what the table is supposed to look like. One should understand the rows should include something with respect to time, and the result that is being measured is the count of the outcomes for each type of outcome. There are some small Excel nuisances such as knowing that inputting items in the "rows" field may yield some default items that don't necessarily add value to the dataset.  

### Analysis of Outcomes Based on Goals

For this analysis, from each campaign, the percentage of successful, failed, and cancelled plays was correlated to the funding goal amount. The scope of the analysis was restricted to the subcategory *plays*. The data was restructured to count the number for a particular outcome within a $5,000 range of a goal. For each goal range, the particular outcome was represented as a percentage of the overall plays in that same range. From this subset, the line chart illustrated below was generated to visualize the relationship between the goal-amount ranges on the x-axis and percentage of successful, failed, and cancelled projects on the y-axis. 

![Outcomes vs. Fund Goals](Resources/Outcomes_vs_Goals.png)

The percentage of successful campaigns depicts no discernable pattern. The percentage of the `successful outcomes in comparison to the goal amount can be observed to be inverse up to $30,000`; however, this pattern changes briefly between $30,000 to $45,0000, followed by a sharp decline for anything larger. The percentage of `failed campaigns shows positive correlation up to $30,000`; however, this pattern also ceases beyond that range. In reviewing the successful and failed outcomes simulatenously, it can be observed that it almost symmetrical in nature, which is a logical observation given they a diametrically opposed percentages of a whole. The percentage of cancelled outcomes is null within the constraints of this analysis. 

The challenge with this particular activity is rooted in understanding how functions operate in Excel. The challenge in using the 'COUNTIFS()' function was observed in the syntax for which it reads "greater than or equal to." In the original input, the signs should be typed as they are read outloud, meaning that the "equal" sign should always come after the angle bracket. Otherwise, the equation will yield a null result.

---

## Results

### Results of Outcomes Based on Launch Date

Based on the data provided for the theater outcomes, there's some conclusions that can be drawn from this visualization. First, between the months of April and August, there are significantly more campaigns being resulted successful. The average of the sucessful theater campaigns is approximately 70. The month of April results in 70 and the month of August results in 72. The months in between these are even higher in their success. The failure rate for the campaigns is consistent throughout this particular range of months, and shows no sign of dependence to the success outcome. Therefore, campaigns started in these months have a higher chance of being successful. 

Another observation can be made about the relationship between successful and failed. Throughout the entire year, the number of successful outcomes has always outweighed the number of failed outcomes. In fact, account for the difference between successful and failed for each month results in average delta of approxitmately 29, and the rate of this delta over time declines after the month of May. It's not until the month of December that the number of sucessful and failed are nearly equal with only a delta of 2 outcomes in December. In comparing the overall trend with duality of the outcomes to each other, it can be concluded that the winter months are the least desired times to start launching campaigns. While it can be argued that people are more inclined to be indoors and participate in more indoor activities such as theaters during these months, the data suggests that the launching a campaign is not ideal.

### Results of Outcomes Based on Goals

Irregardless of the timing of a campaign's launch, it is also fruitful to understand if there are relationships associated with the monetary goals set. In observance of the plays and their outcomes from the figure provided, it can be concluded that having a smaller goal is afforded a more sucessful outcome. The relationship of the delta between failed and successful is inversely related, and the two lines intersect at the range of $15,000 to $20,000. It can be observed that goals below this range have shown to be a lot more successful in gaining pledges that meet or exceed their goal. However, beyond this point, the data has shown the success is less certain with failed outcomes being more significant than successful. The only range for which this logic falters is between $35,000 and $50,000. It can be understood that this discrpenacy can be no less than a coincidence in the grand scheme of the pattern, but more analysis would be needed to ascertain this.

---

## Limitations of the Dataset

The immediate limitations of this dataset are that it is not possible to extrpolate a conclusion from a subcategory-filtered dataset to all subcategories. The outcomes of theaters and plays observed in this report should provide useful insight for those respective campaigns; however, it would not be logical to take the same conclusions and apply them to another category such as film. It is critical to understand this fundamental so that the data can speak to precisely the story that needs to get told. 

There is also a need to better understand other factors that may make a campaign more succesful than others. Justifying a campaign based on date and goals alone do not provide a complete picture of what makes the campaign so succesful. For example, perhaps the data sample was provided for regions where the affinity for art and theater are greater than in other regions. Moreover, perhaps the dataset was taken from campaigns in regions with more affluent pledgers, so geographic and socioeconomic factors are something that are not included in this dataset. It's important to measure the quality and background to the data provided so that there are no inherent skews in the statistics that would therefore draw unfounded conclusions. 

## Possible Areas of Research

There are a variety of other visualizations that can be made from this data. One such visualization that would be interesting would be the pledge amount with respect to time. This can help understand if there were certain periods that the campaigns received higher pledges, and further how much more did contributors pledge than to the goal. It's important to understand the delta between the goal and the pledge amount for any underlying relationships. 

Another filter that could be applied is restricting the datasets to certain countries. Perhaps more affluent countries like the U.S. or Great Britain have greater success rates than other countries. Other factors included in this data set can that could have an effect on the outcome include the backer count or the staff pick columns. Did the amount of backers have a relationship to the campaign being successful? Did the average of the pledge amount with respect to the backer count change over time. Or did the campaign being a staff pick make it much more likely to succeed than if it wasn't a staff pick? These are questions that the researcher can continue to delve from the information embedded. But for the purposes of this report, the scope is limited to the outcomes associated with monetary goals and timing.
