FROM swift:3.1.0

MAINTAINER muukii <m@muukii.me>

WORKDIR /local

RUN apt-get -q update
RUN apt-get -q install -y zip unzip wget

ENV TAG master 

RUN git clone --depth=1 -b $TAG https://github.com/apple/swift-protobuf.git
RUN cd ./swift-protobuf && swift build --configuration release

ENV PROTOC_ZIP protoc-3.2.0-linux-x86_64.zip

RUN wget https://github.com/google/protobuf/releases/download/v4.2.0/$PROTOC_ZIP
RUN unzip $PROTOC_ZIP -d ./protobuf
RUN rm -rf $PROTOC_ZIP

WORKDIR /
ENTRYPOINT ["/local/protobuf/bin/protoc", "--plugin=/local/swift-protobuf/.build/release/protoc-gen-swift"]
