1. The algorithm I used is based on the similarity of users. For a user u, to predict what user u will rate a movie, the algorithm takes the top ten most similar user to user u and takes the average rating of the ratings from the top ten users of the specified movie. If a most similar user has not rated the movie, don’t include him/her.

2. Ran z.run_test(k)
k = 10 received .3655 error, .3357 stddev, .496 rms 
k = 100 received 0.2934 error, .4034 stddev, .4988 rms
 

3. Benchmark 
Took 1.8631045818328857 seconds to run z.run_test(k), where k = 10 
Took 18.443054676055908 seconds to run z.run_test(k), where k = 100 
For some reason my predict method is taking a long time. My predict method loops through the rating data set. If k is ten times greater than its original value, we expect it to run 10 times slower because the time is linear. This is definitely very inefficient because an array is used to store each user id,movie id, rating, and prediction. 

4. I think my project could capture what specific users look for in a stock and show information about related stocks. It can predict and show what the user is looking for so the user does not have to look for it.

https://codeclimate.com/repos/52e5ba16e30ba00c7f0002ab/MovieData