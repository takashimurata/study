docker

// 例

version: '3'
services:
  app:
    image: 'node:14.13.10stretch'
    ports:
      - '3000:3000'
    volumes:
      - .:/myapp
    working_dir: /myapp
    tty: true
  db:
    image: 'mysql:8'
    ports:
      - '3306:3306'
    environment:
      MYSQL_ROOT_PASSWORD: password
