# Introduction #

This is meant as a short 'how to guide' on how to implement your own custom Writer. Be sure to checkout the **PacketMultibroadcasterDemo** in the downloads since is has several sample implementations.


# Details #

  1. Create a custom class that will be used to encode your media and make it extend Writer.
  1. In the constructor pass in the `outputDirectory`, `filename`, `extension`, and `type` of Writer that your trying to write to.
  1. Override the `encodeAudio (AudioPacket $packet)` and/or `encodeVideo (VideoPacket $packet)` function with your own implementation depending on your Writer type.
  1. If you need additional tie-ins to the framework override `setupProcessing()`, `beginProcessing()`, `stopProcessing()`, and/or `finalizeProcessing()` but be sure to call the `super` version of these methods before you write your implementation for validation purposes.