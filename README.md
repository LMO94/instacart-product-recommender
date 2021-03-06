# π₯ Instacart Product Recommender

## βΉοΈ General Information 
The project was part of the 2487-S2 Machine Learning course for the MSc in Business Analytics taught at Nova School of Business and Economics. The topic and scope of the project could be freely chosen by the students, based on given datasets.

### π¨βπ» Group members
- Frederik SΓΈegaard - 44898
- Lennart Max Oser - 44379
- Niclas Frederic Sturm - 45914

## π‘ About the project
This repository contains the prototype of a product recommender based on data from online grocer [Instacart](https://www.instacart.com/ "Instacart's Homepage"). 

The goal was to first **identify a business problem** faced by e-commerce comapnies such as Instacart, second **explore the avaialble data** to get an understaning of what we can work with and then finally prototype a product recommendation engine based on the products in the basket of a used. In addition to the jupyter notebooks, we also created a **Command Line Interface (CLI)** to play around with our built recommendation engine. On top of that, we also created **an API** to demonstrate how such an engine could be used as a Microservice within a company (i.e. Instacart). 


## π Files overview

We divided the project in total of 6 parts numbered from `0` to `5`. Additionally, there is a data folder which has to be created following the instructions below. Here you find an overview of the strucure:
```bash
βββ 0_Introduction                         # containing the business to ML problem part
βΒ Β  βββ 0_Introduction.ipynb
βββ 1_Exploratory_Data_Analysis            # classical EDA based on the six available data sets  
βΒ Β  βββ 1_exploratory_data_analysis.ipynb
βββ 2_Clustering                           # containing the feature engineering, a PCA and the actual clustering alorithm
βΒ Β  βββ 2_clustering.ipynb
βββ 3_Item2Vec                             # containing the Item2Vec alogrhitm and the testing of the recommender engine
βΒ Β  βββ 3_0_Item2Vec.ipynb
βΒ Β  βββ 3_1_Recommendation_Testing.ipynb
βββ 4_Command_Line_Interface               # containting the python file for CLI handling
βΒ Β  βββ CLI_Specification.md
βΒ Β  βββ recommend_me_something.py
βββ 5_Recommender_API                      # contatining the API
βΒ Β  βββ API_Specification.md
βΒ Β  βββ engine
βΒ Β  βΒ Β  βββ recommender_engine.py
βΒ Β  βββ recommender_api.py
βββ data                                   # data folder with all the requried data files
βΒ Β  βββ aisles.csv
βΒ Β  βββ departments.csv
βΒ Β  βββ order_products__prior.csv
βΒ Β  βββ order_products__train.csv
βΒ Β  βββ orders.csv
βΒ Β  βββ products.csv
βΒ Β  βββ sample_submission.csv
βββ environment.yml
βββ README.md
```

## π» Usage
In order to run the code in the same environment as we did please create a virtual environment running the command `conda env create -f environment.yml`. 

After doing so, you should be able to choose the new environment called `instacart` in your preferred IDE.

#### To download the data run the following steps:
1. In your CLI run `mkdir data` or manually create a folder called `data`
2. Run `cd data` in your CLI to get in the right directory
3. Now run the following command to download the data `kaggle competitions download -c instacart-market-basket-analysis`. If you prefer to manually download the data click [here](https://www.kaggle.com/c/instacart-market-basket-analysis/data "Instacart data download)")
4. Extract the zip files using the CLI or what ever method you prefer
