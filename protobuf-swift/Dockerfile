FROM swiftdocker/swift:3.0.2

MAINTAINER muukii <m@muukii.me>

WORKDIR /local

RUN apt-get -q update
RUN apt-get -q install -y zip unzip wget

ENV SWIFT_PROTOBUF_TAG 0.9.26
ENV PATH $PATH:/local/swift-protobuf/.build/release/protoc-gen-swift

RUN git clone --depth=1 -b $SWIFT_PROTOBUF_TAG https://github.com/apple/swift-protobuf.git
RUN cd ./swift-protobuf && swift build --configuration release

RUN wget https://github.com/google/protobuf/releases/download/v3.2.0/protoc-3.2.0-linux-x86_64.zip
RUN unzip protoc-3.2.0-linux-x86_64.zip -d ./protobuf
ENV PATH $PATH:/local/protobuf/bin/protoc

ADD . /proto
WORKDIR /proto

ENTRYPOINT ["/local/protobuf/bin/protoc"]
