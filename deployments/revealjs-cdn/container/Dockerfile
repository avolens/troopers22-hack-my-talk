FROM node@sha256:2d085d25d573a58266319362f32e978f94e06214a62fae15c02d4c4f0567b64f

RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install -y git

RUN git clone https://github.com/hakimel/reveal.js.git /reveal.js
WORKDIR /reveal.js
RUN npm install

COPY tr22.css dist/theme/tr22.css

ADD img/ img/

EXPOSE 8000

CMD ["npm", "start", "--", "--host=0.0.0.0"]
