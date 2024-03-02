FROM easypi/scrapyd

RUN playwright install --with-deps chromium \
    && mv /root/.cache/ms-playwright /ms-playwright \
    && mv /ms-playwright/chromium-* /ms-playwright/chromium \
    # && mv /ms-playwright/firefox-* /ms-playwright/firefox \
    # && mv /ms-playwright/webkit-* /ms-playwright/webkit \
    && chmod -Rf 777 /ms-playwright

RUN mkdir spiders
COPY ../spiders /spiders