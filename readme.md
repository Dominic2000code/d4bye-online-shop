# Online Shop

An online shopping site

## Getting Started

python version 3.11.0

```bash
git clone https://github.com/Dominic2000code/d4bye-online-shop.git

python -m venv venv

source venv/bin/activate

pip install -r requirements.txt

python manage.py migrate

python manage.py createsuperuser

python manage.py runserver
```

### Celery and rabbitMQ

```bash
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:management

celery -A myshop worker -l info
```

### stripe setup

``` bash
brew install stripe/stripe-cli/stripe

stripe login

stripe listen --forward-to localhost:8000/payment/webhook/
```

- You must have weasyprint installed locally on device <https://doc.courtbouillon.org/weasyprint/stable/first_steps.html>

The site will be available at <http://127.0.0.1:8000/>
