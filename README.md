 Flask App on AWS Elastic Beanstalk
Overview

The project successfully deployed a Flask web application featuring a simple login and registration system on AWS Elastic Beanstalk. Leveraging Flask, HTML, JavaScript, CSS, and MySQL, the deployed application allows users to register, log in securely, and access a personalized home page.
Deployment Details
1. Application Configuration:

    The Flask application was configured to bind to 0.0.0.0 and use the appropriate port for AWS Elastic Beanstalk compatibility.

    python

    if __name__ == '__main__':
        app.run(host='0.0.0.0', port=5000, debug=True)

2. Requirements File:

    A requirements.txt file was generated, listing the Python packages required for the application.

    makefile

    Flask==1.1.2
    Flask-MySQLdb==0.2.0

3. AWS Elastic Beanstalk Configuration:

    The AWS Elastic Beanstalk environment was initialized using the EB CLI, and an Elastic Beanstalk application and environment were created.

    bash

    eb init -p python-3.x your-app-name
    eb create your-environment-name

4. Environment Variables:

    Environment variables were configured in the AWS Management Console for the Elastic Beanstalk environment to securely store sensitive information.
        MYSQL_HOST: Your MySQL host address.
        MYSQL_USER: Your MySQL username.
        MYSQL_PASSWORD: Your MySQL password.
        MYSQL_DB: Your MySQL database name.
        FLASK_ENV: Set to production.

5. Deployment:

    The application was deployed to AWS Elastic Beanstalk using the EB CLI.

    bash

eb deploy

The deployed application was opened in a web browser.

bash

    eb open

Conclusion

The Flask application is now successfully hosted on AWS Elastic Beanstalk, providing a scalable and reliable environment for users to interact with the login and registration features. Security measures have been considered, including the use of environment variables for sensitive information.
Next Steps

    Monitor and maintain the Elastic Beanstalk environment.
    Implement additional features and enhancements.
    Conduct regular security assessments and updates.
