# Global Methane Flux Analysis 

**Global Methane Flux Analysis** is a comprehensive data analysis tool designed to streamline Methane Emission data exploration, analysis, and visualisation. The tool supports multiple data formats and provides an intuitive interface for both novice and expert environmental data scientists.

# ![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)


## Dataset Content
The dataset is named "Global Emissions", from [Kaggle]( https://www.kaggle.com/datasets/ashishraut64/global-methane-emissions). It consists of 9 columns x 1548 rows, it is 620.72 kB in size.<br />


 The nine columns consist of:
  1. Index
  2. region 
  3. country - Country of Emission.
  4. emissions - Methane Emissions in kt.
  5. type - Sector from which emissions occur.
  6. Segment- Sub-sector from which emissions occur.
  7. reason - The reason for the emission.
  8. baseYear - Base year for the tracking of emissions.
  9. notes - The source of data


## Business Requirements
Our mission is to analyse, monitor and reduce the Methane Emissions globally, by monitoring the data sources from Satellite observations and Energy and Oil providers. <br />    
Reducing Methane Emissions forms part of the UN Sustainable Development Goals (SDGs), where over 150 countries pledged to reduce emissions by 30% by 2030. <br />
Let us provide you with the data intelligence to help you track and reduce your Methane emission rate.  


## Hypothesis and how to validate?
Investigation Questions:

   - Which countries or regions contribute the most to methane emissions? 
      - Answer: 
         - Countries: China, United States, India, Russia and Brazil
         - Region: Asia Pacific
   - How do developed vs. developing countries compare in methane output?
      - Answer: Developed countries compare more in their Methane Gas outputs.
   - Who are the top 5 methane-emitting countries in the most recent year?
      - Answer: China, United States, India, Russia and Brazil
   - Who are the bottom 10 methane-emitting countries in the most recent year?
      - Answer: Seychelles, Liberia, Gambia, Brunei, Guinea-Bissau,Slovenia,Estonia,Togo,Guyana,Lebanon
   - Does the highest emitting country participate in uncontrolled releases of Methane Gas in the atmosphere?
      - Answer: Yes, China does so in onshore oil, onshore gas and offshore gas productions. Shown in "vented" red coloured in the graph named 'China Energy Emissions by Extraction and Reason'.
   - Which sector(Energy, Waste and Agriculture) produces the most Emissions?
      - Answer: Energy sector
   - Which continent produces the highest Methane Emissions?
      - Answer: Asia

<br />
Validating investigation questions:

   - After cleaning the dataset and removing columns and data that was not necessary, visualisations in the form of an interactive bar chart, mapbox and pie chart was created to compare the total emissions in Energy, Waste and Agriculture of all the countries, continents and top 5 and lower 10 countries emitting Methane Gas.
 

## Project Plan
* Outline the high-level steps taken for the analysis:
   - Data Cleaning
   - Statistical Analysis
   - Exporting Clean Data
   - Visualisations of dataset
      - Bar chart representing Global Emissions
      - Bar chart of top 5 countries
      - Bar chart of lower 10 countries
   - Addressing investigation questions

* How was the data managed throughout the collection, processing, analysis and interpretation steps?

   Cleaning Stage:
   - The dataset from Kaggle was clean, however there were 2 columns I removed (Unnamed:0 and Notes), I found that was not necessary for this project.
   - I also dropped last 5 highest values where "region=world" and "country=world" and "segment=total" as these were summation values of calculations done within the dataset.
   - I dropped rows where "region= world" as this did not represent any country 
   - The generalised rows with "country=European Union" for example were all left within the dataset as I wanted to display these values in my visualisations later.
   - The "segments=total" was not removed as it would have removed valuable data, not all rows were totalled, only the "type=Energy", which meant that the sub items of Energy are duplicated. I resolved this by performing my analysis only on the "Total" values and using the sub items later in the visualisations.

   Analysis Stage:
   - A histogram plot was compared with the 1 variable - "emissions", which showed an asymmetrical skewed distribution.
   - This indicated that most of the data lied towards the left with lower emissions with a few countries on the far right which looked like outliers, however they were not outliers.
   - I then did a logarithmic plot to centralise the data, then the data looked symmetric
   - The mean could not be computed due to the skewness of the data, with one country having rather higher emissions compared to the rest.

   Interpretation Stage:
   - The visualisation stage proved that there were a few high emission countries skewing the distribution.
   - From the investigation, it was also shown that the highest emission country was also emitting Methane uncontrollably and purposely. In my opinion, this is where the analysis is necessary and can provide evidence to prove that Methane Gas is being released uncontrollably, which should be prevented.
   - A geographic map was also plotted which includes all the countries in the world and gives a great visual interpretation globally.
   
* Why did you choose the research methodologies you used?
   - I am interested in this topic and would like to pursue a career as an Environmental Data Scientist. It is important to preserve the environmental for future generations. This is why this research appealed to me.

## The rationale to map the business requirements to the Data Visualisations

* List your business requirements and a rationale to map them to the Data Visualisations
   - The business requirements were to investigate and perform data analysis to understand and interpret Methane Gas emissions to assist countries to reduce their emission rate by 30% by 2030. 
   - Visualisations using maps, bar charts and pie charts were used to answer investigative questions in determining how much Methane Gas was emitted. 
   - Energy, Waste and Agricultural sections were responsible for Methane Gas emissions and was proven in the stacked bar charts.


## Analysis techniques used
* List the data analysis methods used and explain limitations or alternative approaches.
   - I checked the spread of the data and plotted histograms and scatterplots to understand the distribution.
   - The data was asymmetrical which means that most of the values lie towards the left curve. This is a good and bad sign, good because it shows that most countries have low emission rates and bad because there could be outliers that are not outliers. This proved to be correct, the highest emitting country (China) was skewing the data.
   - My limitations was that I only had 1 variable to work with and next time I should better understand the data before I choose it. 
   - The "baseYear" column did not contain data for all 3 years, this was going to prevent me from doing time series analysis, but I worked around it and included the "year" information within the hovering data properties of the plotly graphs.
   - There were also non-country/grouped values inside the "country" column, which proved troubling when doing a latitude/longitude mapbox plot. I overcame this by finding the middle coordinate of the countries that were grouped. 
* How did you structure the data analysis techniques. Justify your response. Did the data limit you, and did you use an alternative approach to meet these challenges?
   - I was restricted because of 1 variable so I couldn't do a heatmap plot and because of the skewness in the distribution

* How did you use generative AI tools to help with ideation, design thinking and code optimisation?
   - No, there was not enough time.

## Ethical considerations

* Were there any data privacy, bias or fairness issues with the data?<br />
   - No, there were no data privacy or bias issues with the data.

* How did you overcome any legal or societal issues?

   - The responsibility of providing accurate and correct Methane emission data is of high importance. It plays a huge role in Climate justice in order to protect the most vulnerable low income communities and countries. 
 <br />Methane gas is a powerful greenhouse has, more potent than CO₂ over 20 years. Reducing emissions has an immediate cooling effect and is one of the fastest ways to slow down global warming.
 <br />It is our goal to flag organisations that are irresponsible in emitting Methane gas. The Planet belongs to all of us and not only large organisations that choose to misuse it. 

## Unfixed Bugs
* Please mention unfixed bugs and why they were not fixed. This section should include shortcomings of the frameworks or technologies used. Although time can be a significant variable to consider, paucity of time and difficulty understanding implementation are not valid reasons to leave bugs unfixed.
   - Feature engineering was not used, if I had more time, I could have tried the rare feature encoder, however with the current data, it would have been hard to structure this as the "segment=total" column had to be left behind, which meant that there was duplicate data within the data.
* Did you recognise gaps in your knowledge, and how did you address them?
   - I consulted with John and Vasi and also used ChatGPT in some areas when I got stuck.
* If applicable, include evidence of feedback received (from peers or instructors) and how it improved your approach or understanding.
   - It assisted me to understand my timeline and also helped me with my approach to managing the data analysis of the project. I was unsure when my dataset would be completely "clean". I was unsure if I should have kepted the "segments=total" as this was duplicated, in the end I decided to keep it because it would have removed important values related to Waste and Agriculture in the dataset. As Waste and Agriculture did not have sub items and only "total" values. 

## Development Roadmap
* What challenges did you face, and what strategies were used to overcome these challenges?
   - I had challenges in understanding if data was truly outliers or if it should have been included. I consulted with John and I made a decision in the end to keep them.
* What new skills or tools do you plan to learn next based on your project experience? 
   - I want to use feature engineering more in the next project.


## Main Data Analysis Libraries
* Here you should list the libraries you used in the project and provide an example(s) of how you used these libraries.
   - Pandas - reading the data in a table format
   - Seaborn - boxplot checking the dispersion of data and outliers
   - Matplotlib - pie chart displaying which continent emits the largest amount of methane gas
   - Plotly express - mapbox of global missions


## Credits 

* In this section, you need to reference where you got your content, media and extra help from. It is common practice to use code from other repositories and tutorials, however, it is important to be very specific about these sources to avoid plagiarism. 
* You can break the credits section up into Content and Media, depending on what you have included in your project. 

   -  External references from the Kaggle dataset "Methane Emissions" on column "notes:"

      -   Average based on United Nations Framework Convention on Climate Change (UNFCCC) (2022), Greenhouse Gas Data Interface, available at: https://di.unfccc.int/; O'Rourke, P. R, Smith, S. J., Mott, A., Ahsan, H., McDuffie, E. E., Crippa, M., Klimont, S., McDonald, B., Z., Wang, Nicholson, M. B, Feng, L., and Hoesly, R. M. (2021, February 05). Community Emissions Data System (CEDS) v-2021-02-05 Emission Data 1975-2019 (Version Feb-05-2021). Available at: http://doi.org/10.5281/zenodo.4509372.; Crippa, M., Guizzardi, D., Solazzo, E., Muntean, M., Schaaf, E., Monforti-Ferrario, F., Banja, M., Olivier, J.G.J., Grassi, G., Rossi, S., Vignati, E. (2021), GHG emissions of all world countries - 2021 Report, EUR 30831 EN, Publications Office of the European Union, Luxembourg, 2021, ISBN 978-92-76-41547-3, doi:10.2760/173513, JRC126363; (2022) EDGAR - Emissions Database for Global Atmospheric Research (EDGAR) v7.0 Greenhouse Gas Emissions. European Commission, Joint Research Centre (JRC) [Dataset] PID: https://edgar.jrc.ec.europa.eu/dataset_ghg70; Climate Watch (2022), Food and Agriculture Organisation of the United Nations (2022). Climate Watch data: Climate Watch, 2022, GHG Emissions, Washington, DC: World Resources Institute. FAO 2022, FAOSTAT Emissions Database. Available at: https://www.climatewatchdata.org/ghg-emissions"   

      -  Estimates from end-uses are for 2020 or 2021 (IEA, Greenhouse gas emissions from energy, 2022, https://www.iea.org/data-and-statistics/data-product/greenhouse-gas-emissions-from-energy)

    - ChatGPT was used together with my code to optimise certain parts
    - The scatter plot in the ETL was code used from John in order to visualise the data
 



## Acknowledgements (optional)
* Thanks to John, Vasi and my husband for their support.
