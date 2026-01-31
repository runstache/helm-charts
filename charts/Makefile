OUTPUT_DIR := ./packages

.PHONY: all package deploy clean

all: package deploy

package:
	mkdir -p ${OUTPUT_DIR}
	helm package bill-api --destination ${OUTPUT_DIR}
	helm package iceberg-catalog --destination ${OUTPUT_DIR}
	helm package nfl-stats-api --destination ${OUTPUT_DIR}
	helm package postgres --destination ${OUTPUT_DIR}
	helm package rss_reader --destination ${OUTPUT_DIR}


deploy:
	cd ${OUTPUT_DIR} && helm repo index --url ${HELM_SERVER}
	mc cp ${OUTPUT_DIR}/ minis3/helm-charts

clean: 
	rm -rf $(OUTPUT_DIR)

