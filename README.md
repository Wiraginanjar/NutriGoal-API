
<h1 align="center" style="font-weight: bold;">NutriGoal: A Machine Learning-Powered Health & Nutrition App</h1>

<p align="center">
<a href="#tech">Technologies</a>
<a href="#started">Getting Started</a>
<a href="#routes">API Endpoints</a>
<a href="#colab">Collaborators</a>
<a href="#contribute">Contribute</a> 
</p>


<p align="center">NutriGoal is a health and wellness application designed to address the growing obesity rates in Indonesia, where **6.53% of men** and **29.7% of women** are classified as obese as of 2024. By leveraging machine learning, NutriGoal aims to provide accessible nutritional guidance to users, especially those in communities with limited access to dietary support.

The app uses **Body Mass Index (BMI)** to assess weight status and offers personalized diet plans to promote healthier lifestyles and reduce obesity-related health risks such as heart disease and diabetes.</p>


<p align="center">
<a href="https://github.com/orgs/Nutrigoal/repositories">📱 Visit this Project</a>
</p>

<h2 id="technologies">💻 Technologies</h2>

- **Javascript**: Core language for data processing and API Connector.
- **HapiJS**: Backend framework for building the API.
- **MySQL**: Database management.
- **Firestore**: Database management.

<h2 id="started">🚀 Getting started</h2>

For run this project locally, please look out below here:

<h3>Prerequisites</h3>

Here the prerequisites for deploy the api:

- [NodeJS](https://github.com/)
- [Git 2](https://github.com)

<h3>Cloning</h3>

How to clone your project

```bash
git clone https://github.com/Nutrigoal/Nutrigoal-CC.git
```

<h3>Config .env variables</h2>

Use the `.env.example` as reference to create your configuration file `.env` with your AWS Credentials

```yaml
# Environment variables.
STATUS=production
#Development port
DEV_PORT=7000
#Production port
PROD_PORT=8000

#DB CONFIG
HOST_DB={YOUR_HOST_DB}
USER_DB={YOUR_USER_DB}
PASSWORD_DB={YOUR_PASSWORD_DB}
DB={YOUR_DB}
DIALECT=mysql
```

<h3>Starting</h3>

How to start your project

```bash
cd Nutrigoal-CC
npm install
npm run start
```

<h2 id="routes">📍 API Endpoints</h2>

Here you can list the main routes of your API, and what are their expected request bodies.
​
| route               | description                                          
|----------------------|-----------------------------------------------------
| <kbd>POST /predict</kbd>     | get predict data from ML API [response details](#post-predict-detail)
| <kbd>GET /history</kbd>     | retrieve data from firestore database [request details](#post-history-detail)
<kbd>GET /history/{documentID}</kbd>     | retrieve data from firestore database by ID [request details](#post-historybyID-detail)

<h3 id="post-predict-detail">POST /predict</h3>


**REQUEST**
```json
{
"activity_level":1,
"age":20,
"diet_category":"vegan",
"food_preference":["Durian","Jackfruit","Passionfruit"],
"gender":1,
"has_gastric_issue":true,
"height":170.0,
"weight":70.0
}
```

**RESPONSE**
```json
{
"favorite_food_name": {
        "ffn_created_at": "2024-12-13T03:45:20.219752",
        "ffn_id": 3,
        "ffn_name": [
            "Durian",
            "Jackfruit",
            "Passionfruit"
        ],
        "ffn_updated_at": "2024-12-13T03:45:20.219752"
    },
  ...
}
```

<h3 id="post-history-detail">GET /history</h3>

**RESPONSE**
```json
{
        "gender": true,
        "perDay": [
            {
                "foodPreference": [
                    "Avocado",
                    "Coconut"
                ],
                "foodRecommendation": [
                    {
                        "protein": 4.300000190734863,
                        "fat": 6,
                        "name": "panipopo samoan sweet coconut buns ",
                        "calories": 218.39999389648438,
                        "id": "01baa666-1aff-4287-9cb7-35258c14bd18",
                        "carbohydrate": 37.099998474121094,
                        "stability": 0
                    },
        ...
}
```
<h3 id="post-historybyID-detail">GET /history/{documentID}</h3>

**RESPONSE**
```json
{
        "gender": true,
        "perDay": [
            {
                "foodPreference": [
                    "Avocado",
                    "Coconut"
                ],
                "foodRecommendation": [
                    {
                        "protein": 4.300000190734863,
                        "fat": 6,
                        "name": "panipopo samoan sweet coconut buns ",
                        "calories": 218.39999389648438,
                        "id": "01baa666-1aff-4287-9cb7-35258c14bd18",
                        "carbohydrate": 37.099998474121094,
                        "stability": 0
                    },
        ...
}
```

<h2 id="colab">🤝 Collaborators</h2>

<p>Special thank you for all people that contributed for this project.</p>
<table>
<tr>

<td align="center">
<a href="https://github.com/farhahsalsabillah">
<img src="https://avatars.githubusercontent.com/u/188359331?v=4" width="100px;" alt=" Farhah Salsabillah Profile Picture"/><br>
<sub>
<b> Farhah Salsabillah</b>
</sub>
</a>
</td>

<td align="center">
<a href="https://github.com/Wiraginanjar">
<img src="https://avatars.githubusercontent.com/u/78730392?v=4" width="100px;" alt="Wiranto Mohammad Ginanjar Profile Picture"/><br>
<sub>
<b>Wiranto Mohammad Ginanjar</b>
</sub>
</a>
</td>

</tr>
</table>

<h2 id="contribute">📫 Contribute</h2>

Here you will explain how other developers can contribute to your project. For example, explaining how can create their branches, which patterns to follow and how to open an pull request

1. `git clone https://github.com/Nutrigoal/Nutrigoal-CC.git`
2. `git checkout -b feature/NAME`
3. Follow commit patterns
4. Open a Pull Request explaining the problem solved or feature made, if exists, append screenshot of visual modifications and wait for the review!

<h3>Documentations that might help</h3>

[📝 How to create a Pull Request](https://www.atlassian.com/br/git/tutorials/making-a-pull-request)

[💾 Commit pattern](https://gist.github.com/joshbuchea/6f47e86d2510bce28f8e7f42ae84c716)
