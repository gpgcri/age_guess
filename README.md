## About The AgeGuess Project

[AgeGuess dataset](https://www.ageguess.org/download)

[AgeGuess paper](https://www.nature.com/articles/s41597-019-0245-9.pdf)

AgeGuess.org is a simple online game using biological and perceived age as biomarkers to address scientific questions related to aging in humans.

About the data:
* The data on perceived age we present here span birth cohorts from the years 1877 to 2012. 
* The database currently contains around 220,000 perceived age guesses. 
* Almost 4500 citizen scientists from over 120 countries of origin have uploaded ~4700 facial photographs. 
* Beyond studying the ageing process, the data present a wealth of possibilities to study how humans guess ages and who is better at guessing ages.

Variables and description:
* The ag_guess.csv file stores the information regarding the age guesses using the following variables: uid, guess_id, photo_id, ageG, outG, and access. The uid, guess_id, and photo_id variables contain the individual identifiers of the user who made the guess, the guess itself, and the photograph guessed on. The ageG and outG variables describe the guessed age and the deviation in the guess from the real age in years, respectively. The access variables store the timestamp when the guess was made in date and time UTC + 1:00 in the format ‘YYYY-MM-DD HH:MM:SS’. While repeated guessing by the same person on the same photograph is no longer possible due to the current version of the algorithm controlling the photos displayed to the users, this was possible in early implementations of AgeGuess. Data on repeated guesses are available from previous versions of the database upon request.

* The ag_gamers.csv fle stores the information regarding the users (aka gamers) with the following variables: uid, g, ng, points, gender, ethnicity, birth_country, birth_year, access, and created. Tese variables store the individual identifer of the user (uid), the number of correct guesses the user made (g), the number of other guesses (ng), and the points gained in the online game (points). Furthermore, the fle contains the users’ basic demographic information regarding gender, ethnicity, birth country, and birth year, stored in variables of these names. Finally, the access and created variables store the timestamp in date and time UTC+1:00 of when the user last logged in and of when the user created an account with AgeGuess, respectively.

* The ag_photos.csv file stores the information regarding the photographs using the following variables: uid, photo_id, age, relation, gender, ethnicity, birth_country, birth_year, death_age, and created. The uid and photo_id variables represent the individual identifiers the user who uploaded the photograph and of the photograph. The relation variable indicates whether the photograph is of the user or of another person to which the user has a relation (categories: user, unrelated of friend, mother/father, son/daughter, sibling, half sibling, maternal/paternal grandparent, maternal/paternal aunt/uncle, maternal/paternal cousin, grandchild). The gender, ethnicity, birth_country, birth_year, death_age variables contain the respective basic demographic information for the person in the photograph. The created variable stores the timestamp when the photograph was added in date and time UTC + 1:00 in the format ‘YYYY-MM-DD HH:MM:SS.

### Built With

This project was made in Google Collab and the used Python packages were:
* [Pandas](https://pandas.pydata.org/pandas-docs/stable/index.html)
* [Matplolib](https://matplotlib.org/stable/index.html)
* [Seaborn](https://seaborn.pydata.org/)


## Getting Started

This section shows some key points in the project.

### Prerequisites

This is an example of how to list things you need to use the software and how to install them.
* download the data
  ```sh
  !curl https://www.ageguess.org/download/data --output ageguess-data-public-csv-20190530--.zip
  ```
* unzip file
  ```sh
  !unzip ageguess-data-public-csv-20190530--.zip
  ```
* load csv
  ```sh
  ag_guess_df = pd.read_csv(r'AgeGuessDataUKDataService I/ag_guess.csv')
  ```
* import libraries
  ```sh
  import numpy as np 
  import pandas as pd 
  from sklearn import preprocessing
  import matplotlib.pyplot as plt 
  import seaborn as sns
  ```
### Installation

1. Clone the repo
   ```sh
   git clone https://github.com/gpgcri/age_guess.git
   ```
2. Change directory
   ```sh
   cd age_guess
   ```
3. Open the notebook
   ```sh
   jupyter notebook  notebook.ipynb
   ```

## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## License

[GNU General Public License](https://www.gnu.org/licenses/gpl-3.0.en.html#:~:text=%20GNU%20General%20Public%20License%20%201%20GNU,%20...%20To%20%E2%80%9Cmodify%E2%80%9D%20a%20work...%20More%20)


## Contact

Gabriel Perez
