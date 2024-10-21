# Michigan Traffic Crash Data Analysis

## Introduction

This project analyzes traffic accident data from Michigan, utilizing the Michigan Traffic Crash Facts (MTCF) database. The MTCF provides comprehensive crash data and allows users to construct custom queries, view results in various formats, and access historical documents dating back to 1952. This analysis is part of the **NVIDIA LlamaIndex Developer Contest**, aimed at creating innovative applications powered by NVIDIA and LlamaIndex technologies.

## Data Source

The traffic accident data is sourced from the Michigan Traffic Crash Facts website (https://www.michigantrafficcrashfacts.org). The dataset includes detailed information about:

- Crash Date and Time
- Crash Type
- Light Conditions
- Road Surface Condition
- Vehicle Type
- Person Information (Age, Sex, Race, etc.)
- Narrative (unstructured NLP data from police accident reports)

## Project Highlights

1. **Data Cleaning**: Nvidia nemo-curator was applied to remove personal sensitive information from the traffic accident data, particularly from the Narrative column.

2. **Vector Database Creation**: A vector database was created using llama-index. Each row of the dataset is treated as a traffic accident file, with the Narrative as the main body and other columns as metadata.

3. **ChatBot Development**: A chatbot was developed using GPT-3.5-turbo to analyze the traffic accident data and answer various questions.

4. **PII Removal**: Nemo pii_modifier effectively identified and replaced sensitive information, such as person names, in the Narrative column.

5. **Simplified Pipeline**: LlamaIndex streamlined the process of creating and deploying the ChatBot.

## Key Questions Addressed

The ChatBot can answer interesting questions such as:

1. **What are the most common traffic accident patterns?**
   ```diff
   + Rear-end collisions and sideswipe-same incidents are among the most common traffic accident patterns based on the provided context information.
   ```

2. **What is the average age of the drivers involved in the traffic accidents?**
   ```diff
   + The average age of the drivers involved in the traffic accidents is 53.3 years.
   ```

3. **What is the most frequent weather condition when traffic accidents happened?**
   ```diff
   + The most frequent weather condition when traffic accidents happened based on the provided context information is snow.
   ```

4. **What time of day do most accidents occur?**
   ```diff
   + Accidents in the provided context occurred during different times of the day - both during daylight and at night.
   ```

5. **Which vehicle makes are most frequently involved in accidents?**
   ```diff
   + HONDA, FORD, and TOYOTA vehicles are most frequently involved in accidents based on the provided context information.
   ```

## Challenges

A significant challenge was removing personal sensitive information from the traffic accident reports, as victim names sometimes appeared in the Narrative column.

## Next Steps

1. **Expand Dataset**: Currently, the project uses a random sample of 564 traffic accident records from 2022. Expanding this to include more data from the total 293,341 traffic accidents in Michigan would provide more comprehensive insights.

2. **Improve Prompts**: Refine the prompts used in the chatbot for more effective communication with the LLMs.

3. **Explore Other LLMs**: Test and compare the performance of other language models beyond GPT-3.5-turbo.

4. **Enhance Data Analysis**: Utilize the MTCF Data Query Tool to construct more complex queries and gain deeper insights into Michigan crash data.

5. **Incorporate Historical Data**: Leverage the historical documents available on the MTCF website to analyze long-term trends in traffic accidents.

## Conclusion

This project demonstrates the potential of combining advanced NLP techniques with comprehensive traffic accident data to gain valuable insights. By addressing privacy concerns and leveraging powerful language models, we can create tools that assist in understanding and potentially reducing traffic accidents. Participation in the NVIDIA LlamaIndex Developer Contest has provided a platform for innovation using state-of-the-art technologies.