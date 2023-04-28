# workout-tracer-porject
This script allows you to track your exercises by making use of two APIs: Nutritionix API and Sheety API. The Nutritionix API is used to calculate the number of calories burned during the exercises, while the Sheety API is used to store the exercise data in a Google Sheet.

The script starts by asking the user to input the exercises they did. This input is then used as a parameter for the Nutritionix API call, along with the user's personal data (gender, weight, height, and age). The Nutritionix API then returns a JSON object that contains information about the exercises performed, including the exercise name, duration, and number of calories burned.

Next, the script retrieves the current date and time using the datetime module. This information is added to the JSON object returned by the Nutritionix API, along with the exercise data, and then sent to the Sheety API using a POST request.

The Sheety API stores this data in a Google Sheet that is specified by the user. The sheet must be set up beforehand, and the sheet's name and API endpoint must be provided in the code. Authentication is optional, and three methods are provided: no authentication, basic authentication, and bearer token authentication.

If authentication is required, the necessary credentials are stored as environment variables. The code will check for the existence of these variables and use them if they exist.

Overall, this script is a useful tool for anyone looking to track their exercises and monitor their progress over time.
