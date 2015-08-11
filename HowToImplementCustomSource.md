# Introduction #

This is meant as a short 'how to guide' on how to implement your own custom Source. Be sure to checkout the **PacketMultibroadcasterDemo** in the downloads since is has several sample implementations.


# Details #

  1. Create a custom class that will be capture your media and make it extend Source.
  1. In the constructor pass in a 'id' for debugging purposes and the `type` of Source (audio or video)
  1. Override the `packAudioPacket (AudioPacket $audioPacket)` or `packVideoPacket (VideoPacket $videoPacket)` function with your own implementation on how to pack the packet depending on your Source type.
  1. If you need additional tie-ins to the framework override `setupProcessing()`, `beginProcessing()`, `stopProcessing()`, and/or `finalizeProcessing()` but be sure to call the `super` version of these methods before you write your implementation for validation purposes.