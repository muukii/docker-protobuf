FROM swiftdocker/swift:latest

MAINTAINER muukii <m@muukii.me>

RUN git clone https://github.com/apple/swift-protobuf.git ~/local/swift-protobuf
RUN cd ~/local/swift-protobuf
RUN swift build --configuration release
