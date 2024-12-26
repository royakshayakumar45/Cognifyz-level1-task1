# Cognifyz-level1-task1
new repo
{
 "cells": [
  {
   "cell_type": "code",
   "execution_count": 1,
   "id": "703ba396-0555-40d2-b286-37a448ade9ba",
   "metadata": {},
   "outputs": [],
   "source": [
    "import numpy as np \n",
    "import pandas as pd\n",
    "import matplotlib.pyplot as plt #visualizing data \n",
    "%matplotlib inline\n",
    "import seaborn as sns"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 2,
   "id": "c7bc9cc1-c85b-4b43-98e9-f2cdfaddf922",
   "metadata": {},
   "outputs": [],
   "source": [
    "restaurants_df= pd.read_csv(r\"C:\\Users\\Shubham\\Downloads\\cognifyz\\Dataset .csv\",encoding= \"unicode_escape\")"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 3,
   "id": "7f8259de-506b-4235-af45-93e4521a4729",
   "metadata": {},
   "outputs": [
    {
     "data": {
      "text/plain": [
       "(9551, 21)"
      ]
     },
     "execution_count": 3,
     "metadata": {},
     "output_type": "execute_result"
    }
   ],
   "source": [
    "restaurants_df.shape"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "f354fa87-b0d5-49f2-897e-712faf8e6e61",
   "metadata": {},
   "outputs": [],
   "source": [
    "restaurants_df.head()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "id": "c556474e-7691-4475-90e6-69ce47ce614d",
   "metadata": {},
   "outputs": [],
   "source": [
    "restaurants_df.info()"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": 5,
   "id": "74769cf4-875d-41f3-8094-40cb53c99b41",
   "metadata": {},
   "outputs": [
    {
     "name": "stdout",
     "output_type": "stream",
     "text": [
      "Top Three Cuisines:\n",
      "Cuisines\n",
      "North Indian             936\n",
      "North Indian, Chinese    511\n",
      "Chinese                  354\n",
      "Name: count, dtype: int64\n",
      "\n",
      "Percentage of Restaurants Serving Each Top Cuisine:\n",
      "Cuisines\n",
      "North Indian             9.800021\n",
      "North Indian, Chinese    5.350225\n",
      "Chinese                  3.706418\n",
      "Name: count, dtype: float64\n"
     ]
    }
   ],
   "source": [
    "correct_column_name = 'Cuisines'\n",
    "cuisine_counts = restaurants_df[correct_column_name].value_counts()\n",
    "top_cuisines = cuisine_counts.head(3)\n",
    "total_restaurants = len(restaurants_df)\n",
    "top_cuisines_percentage = (top_cuisines / total_restaurants) * 100\n",
    "print(\"Top Three Cuisines:\")\n",
    "print(top_cuisines)\n",
    "print(\"\\nPercentage of Restaurants Serving Each Top Cuisine:\")\n",
    "print(top_cuisines_percentage)"
   ]
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3 (ipykernel)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.13.1"
  }
 },
 "nbformat": 4,
 "nbformat_minor": 5
}
