FROM python:3.13-slim
ENV POETRY_VIRTUALENVS_CREATE=false

WORKDIR /app
COPY . .

RUN pip install poetry
RUN poetry install --no-interaction --no-ansi

EXPOSE 8000
CMD ["poetry", "run", "uvicorn", "vida_project_api.app:app", "--host", "0.0.0.0", "--port", "8000"]
