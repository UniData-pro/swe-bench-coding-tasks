include .env


report:
	git config --global --add safe.directory ${REPO_NAME}
	cd ${REPO_NAME} && git checkout -f ${BASE_COMMIT}
	rm -rf ${REPO_NAME}/.dockerignore
	cp ${PATH_TO_ENV_FILES}/dockerfile ${REPO_NAME}/
	docker compose build
	docker compose up