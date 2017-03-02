FROM swiftdocker/swift:3.0.2

MAINTAINER muukii <m@muukii.me>

WORKDIR ~/local

RUN apt-get -q update
RUN apt-get -q install -y zip unzip wget

ENV SWIFT_PROTOBUF_TAG 0.9.26

RUN git clone --depth=1 -b $SWIFT_PROTOBUF_TAG https://github.com/apple/swift-protobuf.git
RUN cd ./swift-protobuf && swift build --configuration release

RUN wget https://github.com/google/protobuf/releases/download/v3.2.0/protoc-3.2.0-linux-x86_64.zip
RUN unzip protocprotoc-3.2.0-linux-x86_64.zip -d ./protoc
