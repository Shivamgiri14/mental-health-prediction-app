# Mental Health Prediction App

A Flask web application that uses machine learning to predict mental health conditions based on survey responses.

## Features

- **Mental Health Prediction**: Uses a trained Random Forest model to predict mental health treatment needs
- **Interactive Web Interface**: User-friendly forms for data input
- **Data Visualization**: Charts and graphs for data analysis
- **File Upload**: Support for CSV dataset uploads
- **Responsive Design**: Works on desktop and mobile devices

## Technology Stack

- **Backend**: Python Flask
- **Machine Learning**: scikit-learn, Random Forest Classifier
- **Data Processing**: pandas, numpy
- **Frontend**: HTML, CSS, JavaScript
- **Deployment**: Render (with gunicorn)

## Local Development

1. Clone the repository
2. Install dependencies: `pip install -r requirements.txt`
3. Run the application: `python app.py`
4. Access the app at `http://localhost:5000`

## Deployment

This app is configured for deployment on Render using the `render.yaml` configuration file.

## Model Information

The machine learning model is trained on mental health survey data and uses features like:
- Gender
- Employment status
- Family history
- Work interference
- Company size
- Remote work status
- And many other mental health related factors

## Live Demo

🚀 **Deployed Application**: [Coming Soon - Will be updated after deployment]

## Contributing

Feel free to submit issues and pull requests to improve the application.

## License

This project is open source and available under the MIT License.
