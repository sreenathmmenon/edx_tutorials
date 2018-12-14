## Conditions:

**Python - 3**

## Installation and Configuration Steps

1) Create Virtual Environment

```
virtualenv cdelta
```

2) cd cdelta

3) Activate virtual environment

```
source bin/activate
```

4) Clone the Project

```
git clone https://github.com/sreenathmmenon/edx_tutorials
```

5) Enter project directory

```
cd edx_tutorials
cd edx
```
6) Install dependecies

```
pip3 install -r requirements.txt
```


6) Create database
Name - virtual_class
Configure database settings in edx/edx/settings.py

```

DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'virtual_class',
        'USER': 'classUser',
        'PASSWORD': '**********',
        'HOST': 'localhost',   # Or an IP Address that your DB is hosted on
        'PORT': '3306',
    }
}

```

7) Do migration

```
python3 manage.py migrate
```

8) Create Admin User

```
python3 manage.py createsuperuser
```

9) Load Subject data into db(fixtures)

```
python3 manage.py loaddata subjects.json
```
(subjects.json present inside edx/courses/fixtures)

10) Run the server

```
python3 manage.py runserver
```

### Screenshots

**Login Page**

![Login Page](https://github.com/sreenathmmenon/edx_tutorials/blob/master/docs/login.png )


**Course Display**

![Course Display](https://github.com/sreenathmmenon/edx_tutorials/blob/master/docs/course_display.png)


**Course Enrollment**

![Course Enroll](https://github.com/sreenathmmenon/edx_tutorials/blob/master/docs/course_enroll.png )


**Course Registration**

![Course Registration](https://github.com/sreenathmmenon/edx_tutorials/blob/master/docs/course_registration.png)


**Enrolled Courses**

![Enrolled Courses](https://github.com/sreenathmmenon/edx_tutorials/blob/master/docs/my_courses.png)



