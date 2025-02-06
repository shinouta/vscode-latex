FROM paperist/texlive-ja:latest
RUN wget -P "/sty" "https://raw.githubusercontent.com/h-kitagawa/plistings/master/plistings.sty"
RUN tlmgr update --self
RUN tlmgr install algorithms algorithmicx algpseudocodex
RUN apt-get update && \
  apt-get install -y --no-install-recommends \
  git ssh \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*
CMD [ "bin/bash" ]
