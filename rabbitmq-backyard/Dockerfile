FROM rabbitmq:3.7-management-alpine

RUN rabbitmq-plugins enable --offline rabbitmq_mqtt rabbitmq_federation_management

ADD rabbitmq.conf /etc/rabbitmq/rabbitmq.conf
