# Student-clustering-with-KMeans

## Project Overview

**Project Title**: Student Clustering With KMeans & providing real time restaurant recommendations

**Level**: Intermediate  

This project demonstrates the implementation of KMeans Clustering (an unsupervised machine learning algorithm) to make student clusters based on similar eating and spending habits, and then creating a map of their locality with libraries like geopy for geolocation and distance calculations. Using API to get realtime restaurant infomation, we then show nearby restaurants to the students matching their habits. All of the coding is done in Python. 

![students](https://github.com/Saiqua29/Student-clustering-with-KMeans/blob/main/student%20clustering.png)



This script is a complete end-to-end pipeline for:
**Clustering Students Based on Lifestyle and Recommending Nearby Food Venues (in Thane,Mumbai, Maharashtra).**


 ✅ *Summary of What the Code Does*

1.  Uses Geolocation and the Foursquare API to pull food venues around Thane.

 2.  Simulates 1000 students with lifestyle attributes like eating frequency, spending capacity, and food preference.

 3. Performs KMeans clustering on student behavior (eating out and spending).

4. Removes outliers using the IQR method.

5. Uses Elbow Method to decide the optimal number of clusters (in this case, k = 4).

6. Maps each student and venue to a cluster.

7. Creates an interactive map showing:

 - Clustered students

 - Recommended venues for each group

 - Cluster centroids

📦 **Key Libraries Used**
| Library                  | Purpose                                          |
| ------------------------ | ------------------------------------------------ |
| `pandas`, `numpy`        | Data handling and simulation                     |
| `matplotlib`, `seaborn`  | Plotting Elbow graph and clusters                |
| `sklearn.cluster.KMeans` | Clustering students based on normalized features |
| `folium`                 | Interactive map creation                         |
| `geopy`                  | Geolocation and distance calculations            |
| `requests`               | API calls to fetch real venue data               |

🔍 **Explanation**
1. Get Location Coordinates for Thane

   - Uses geopy.Nominatim to fetch the latitude and longitude of "Thane West".

2. Pull Food Venues via Foursquare API

   - Makes a GET request to fetch 20 places within a 2 km radius around Thane.

   - Stores venue name, latitude, longitude, and category.

3. Simulate Student Data

    Creates simulated data of 1000 students with following features:

   - Frequency_of_Eating_Out: [1–10]

   - Spending_Capacity: ₹100–₹1000

   - Food_Preference: Veg, Non-Veg, Vegan

    All students are assigned the same location (Thane,Mumbai) to showcase how students of one area(like from one school/college/coaching) would decide to eat out.

4. Encode Categorical Data

    - Converts food preference into numeric format to prepare for clustering.

5. Normalize Features & Remove Outliers

   - Uses StandardScaler to normalize spending and frequency.

   - Uses IQR to remove outlier students for more accurate clustering.

6. Find Best Number of Clusters (Elbow Method)

   - Computes "inertia" for k = 1 to k = 10.

   - Elbow plot helps visually identify the point of diminishing returns (chosen k = 4).

7. Perform KMeans Clustering

   - Assigns each student to one of 4 clusters.

   - Plots students on a 2D scatter plot with cluster centroids.

8. Map Venues to Clusters

   - Calculates the geodesic distance from each venue to all cluster centroids.

   - Assigns each venue to the nearest student cluster.

9. Generate Interactive Map (Folium)

    Plots:

   - Students as colored circle markers (per cluster)

   - Venues as icons (colored based on assigned cluster)

   - Cluster centroids as black markers

📍 **Final Output**

   Saves an HTML file students_restaurants_map.html.

   You can open it in a browser to explore:

   - Which food places are recommended for which type of student cluster.

   - Geographic distribution of clusters (currently all centralized in Thane but extendable).

 💡 **Why use restaurant cluster centroids?**

   - Represents variety: Restaurants are more spatially spread out.

   - Actionable information: Students can see where the main hubs of restaurant clusters are.

   - Clarity: Prevents map clutter and overlap since student markers are already dense.       

💡 **Future Scope of work**

   - Deploy Map Online 

## Conclusion

This project demonstrates the application of KMeans clustering in solving real world problems. Following skills are demonstarted in this project:

   - Getting latitude & longitude of any location using *geopy*
   - Pulling real time data via API (*webscraping*)
   - Machine learning algorithm of unsupervised learning( *KMeans*)
   - Measuring geodesic distance from each venue to all cluster centroids (*geodesic*)
   - Generating an interactive Map (*Folium*)
  
## Author - Saiqua29 

This project is part of my portfolio, showcasing the SQL skills essential for data analyst roles. If you have any questions, feedback, or would like to collaborate, feel free to get in touch!


### Stay Connected if you'd like to

For more content on SQL, data analysis, and other data-related topics, make sure to follow me on social media:

- **LinkedIn**: [Connect with me professionally](https://www.linkedin.com/in/saiqua-shaikh-b28682124/)

Thank you for your interest in this project!

 
