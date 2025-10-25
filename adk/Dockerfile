FROM python:3.13.9-alpine3.22
# https://hub.docker.com/_/python

ARG WXO_INSTANCE
ARG WXO_API_KEY
ENV WXO_ENV_NAME="wxo-adk"

RUN mkdir /${WXO_ENV_NAME}

WORKDIR /${WXO_ENV_NAME}

RUN pip install --upgrade ibm-watsonx-orchestrate && \
    orchestrate env add -n ${WXO_ENV_NAME} -u ${WXO_INSTANCE} --type ibm_iam && \
    orchestrate env activate ${WXO_ENV_NAME} --api-key ${WXO_API_KEY} 

CMD ["tail", "-f", "/dev/null"]