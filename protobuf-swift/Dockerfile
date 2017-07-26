FROM swift:3.1.0

MAINTAINER muukii <m@muukii.me>

WORKDIR /local

RUN apt-get -q update
RUN apt-get -q install -y zip unzip wget

ENV TAG "0.9.904"

RUN git clone --depth=1 -b $TAG https://github.com/apple/swift-protobuf.git
RUN cd ./swift-protobuf && swift build -c release # -Xswiftc -static-stdlib
RUN cp ./swift-protobuf/.build/release/protoc-gen-swift /usr/local/bin/protoc-gen-swift

RUN wget https://github.com/google/protobuf/releases/download/v3.3.0/protoc-3.3.0-linux-x86_64.zip -O protobuf.zip
RUN unzip protobuf.zip -d ./protobuf
RUN rm -rf protobuf.zip
RUN cp ./protobuf/bin/protoc /usr/local/bin/protoc

ADD . /proto
WORKDIR /proto

ENTRYPOINT ["protoc"]
