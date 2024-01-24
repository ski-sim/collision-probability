## set your Login.ini file
You need to sign up for a space-track account to download the tle data. <br/>
And update your account to the Login.ini file.


# Covariance-using-historical-TLE

![image](https://github.com/SpaceMapR-D/Covariance-using-historical-TLE/assets/121158156/169132e6-7454-4a91-9c73-d8126f2d6f0e)

This code estimates the covariance matrix using historical TLE data.
To achieve covariance, comparison differences between the TLEs are needed. 
The method employed to generate the comparison data involves propagating all of the TLEs in a given time window to specific times, then 
calculating the difference between the estimated state vectors (position,velocity)
The state vector differences are known as residuals.
The residuals and their mean can be used to compute the covariance matrix of the state vector. 


# maximum_collision_probability_2D
![image](https://github.com/ski-sim/collision-probability/assets/121158156/b1b666f7-fab0-4f4e-9997-e66f045bf608)
If we use a low precision covariance, the probability value will be too small to be meaningful . <br/>Therefore, we compute a maximum collision probability that conservatively computes the covariance.<br/>
we have several assumption of error covariance ellipse.<br/>
1. orientation along with major axis.<br/>
2. shape is fixed by aspect ratio which is 3 in this code.<br/>

then, we can calculate Pcmax easily<br/>
For some additional analysis, there is a secondary code that can be used.

### External data sources
TLE :  [https://www.space-track.org/](https://www.space-track.org/) <br/>
Dimension : https://discosweb.esoc.esa.int/ <br/>
TCA : https://celestrak.org/ <br/>
