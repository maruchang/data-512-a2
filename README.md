# data-512-a2
Chang Xu

## Goal

The goal of this assignment is to explore the concept of bias through data on Wikipedia articles - specifically, articles on political figures from a variety of countries. For this assignment, you will combine a dataset of Wikipedia articles with a dataset of country populations, and use a machine learning service called ORES to estimate the quality of each article. <br />

I perform an analysis of how the coverage of politicians on Wikipedia and the quality of articles about politicians varies between countries. Your analysis will consist of a series of tables that show: <br />

1. the countries with the greatest and least coverage of politicians on Wikipedia compared to their population.
2. the countries with the highest and lowest proportion of high quality articles about politicians.
3. a ranking of geographic regions by articles-per-person and proportion of high quality articles.


## Data 
In this project, two datasets are used:

* [The Wikipedia politicians by country dataset](https://figshare.com/articles/dataset/Untitled_Item/5513449) is a dataset that contains politicians by country data, having the fields of:
 1. `page`: title of the Wikipedia article
 2. `country`: country associated with the article
 3. `rev_id`: stands for "revision_id". It is a unique identifier that is generated by revising the articles. We use it to identify the articles

The dataset is downloaded as `/raw_data/page_data.csv`in this repo.
 
* The population data is available in CSV format as `/raw_data/WPDS_2020_data.csv`. This dataset is drawn from the [world population data sheet](https://www.prb.org/international/indicator/population/table/) published by the Population Reference Bureau.



## API
This assignment uses the ORES REST API, and the documentation can be found [here](https://ores.wikimedia.org/v3/#!/scoring/get_v3_scores_context_revid_model)


## Final data file fields
* For `wp_wpds_countries-no_match.csv`: <br />

| Column   |
| ------------- |
| rev_id    |
| score   |
| page    |
| country  |


* For `wp_wpds_politicians_by_country.csv`: <br />

| Column  |
| ------------- |
| country  |
| article_name  |
| revision_id  |
| article_quality_est.  |
| population  |


## Notes for user
The project also aims to explore the Geographic regions by coverage: Ranking of geographic regions in terms of the total count of politician articles from countries in each region as a proportion of total regional population and in terms of the relative proportion of politician articles from countries in each region that are of GA and FA-quality. Unfortunately, due to my initial lack of design in cleaning and merging tables and a lack of time, it is not implemented yet. However, these will be interesting metrics to look at.

## License
This project is under [The MIT License](https://opensource.org/licenses/MIT)
