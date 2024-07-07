# recommander-system-project

Recommander System project by sami.carret

## Data Collection and Preprocessing

For this part, I chose to only use the MovieLens dataset as I had severe memory problems on my computer. I dropped the Timestamp column for this dataset as I judged it not useful for our purpose. This dataset includes 1 million ratings from 6,000 users on 4,000 movies.

## Feature Engineering

I created a user-item interaction matrix in a sparse format without using the pivot method as this method was too heavy on my computer and would simply not work. This approach is memory efficient and suitable for large datasets.

## Model Development

I used the ALS algorithm from the implicit library for collaborative filtering. ALS is well-suited for implicit feedback datasets and scales well with large datasets.

## Recommandation Algorithm

I developed a function to recommend movies for a couple by combining their preferences. The function averages the preferences of the two users to compute a combined score for each movie.

## Evaluation

To evaluate my model, I calculated the RMSE.
After the calculations, I obtained a RMSE of 3.69 which isn't great, this probably stems from the fact the i didn't use all of the features from the dataset because of memory constraints.

## Conclusion

This project demonstrated the development of a movie pairing recommander system using the MovieLens dataset and the ALS algorithm from the implicit library. By focusing on efficient data handling, I built a system that provides relevant movie recommendations for couples. The approach avoids memory-intensive operations like pivot, ensuring scalability for large datasets and a minimal memory usage for weaker machines. Future work could involve incorporating additional features such as movie genres, directors, and cast to further enhance the recommendation quality.