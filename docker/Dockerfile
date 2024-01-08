# See https://hub.docker.com/r/goofball222/pritunl/tags
# 1.32.3746.95
FROM goofball222/pritunl:1.32.3746.95
# https://github.com/simonmicro/Pritunl-Fake-API/commit/86e1fa2ce18017f31906b2b5b4506fe5ffae5d0d
# FROM goofball222/pritunl:1.32.3504.68
# FROM goofball222/pritunl:1.30.3343.47 # NOT FOUND

ARG API_SERVER_DOMAIN=${API_SERVER_DOMAIN:-pritunl-api.simonmicro.de}
ENV API_SERVER_DOMAIN $API_SERVER_DOMAIN

# Yes, you will need to copy it over into the build context...
COPY setup.py .

RUN chmod +x setup.py; python3 -u setup.py --install --api-server ${API_SERVER_DOMAIN:-}; rm setup.py