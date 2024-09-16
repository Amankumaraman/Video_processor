

 Fatmug-Django: Video Processing Platform

This project provides a web application that allows users to upload videos, process them in the background to extract subtitles, and display these subtitles as closed captions. The application supports multiple language subtitles and includes search functionality within the video subtitles.

 Features
- Video upload and processing
- Subtitle extraction using `ccextractor`
- Search functionality within video subtitles
- Django admin interface for video management
- Dockerized for easy deployment
- PostgreSQL integration for subtitle storage

 Prerequisites

- Python 3.12+
- Django
- PostgreSQL
- Docker & Docker Compose
- FFmpeg (for video processing)
- Other dependencies are listed in `requirements.txt`

 Database Configuration

To configure the PostgreSQL database credentials, create a `.env` file in the project root directory. The file should have the following structure:

bash
DATABASE_NAME=videodb             
DATABASE_USER=postgres         
DATABASE_PASSWORD=123  
DATABASE_HOST=db
DATABASE_PORT=5432


Make sure the credentials match your PostgreSQL setup or the ones provided in your Docker configuration.

 Installation

 1. Clone the Repository:
bash
git clone https://github.com/Amankumaraman/Video_processor.git
cd Video_processor


 2. Set Up Docker:
Build and run the Docker containers using the following commands:
bash
docker-compose build

bash
docker-compose up -d


 3. Migrate the Database:
Run the migrations to set up the PostgreSQL database:
bash
docker-compose exec django-app python manage.py migrate


 4. Create a Superuser:
To create an admin user, use the following command:
bash
docker-compose exec django-app python manage.py createsuperuser


 5. Access the Application:
- Django Admin interface:  
  `http://127.0.0.1:8000/admin/`  
  (Login using the superuser credentials created earlier)
  
- Video Upload page:  
  `http://127.0.0.1:8000/upload/`

 Usage

- Upload videos via the `/upload/` page.
- The system processes the video to extract subtitles and stores them in the database.
- Subtitles can be searched and displayed alongside the video as closed captions.

 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
#Amankumar
