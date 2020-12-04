ARG ODOO_IMAGE=odoo:14
FROM ${ODOO_IMAGE}
USER root
COPY requirements.txt /tmp/
RUN pip3 install -r /tmp/requirements.txt
USER odoo