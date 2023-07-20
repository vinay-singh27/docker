# Use an existing docker image
FROM alpine

# install dependenicies
RUN apk add --update gcc
RUN apk add --update redis

# Tell the image what to do when the container starts
CMD ["redis-server"]
