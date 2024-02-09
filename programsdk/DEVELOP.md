Here is what you should know about developing tools using framework

-Do NOT use imgui functions directly and instead create UI descriptors manually or through the ui editor tool
-Always export your actual entrypoint in the following format:
    void ModtoolMain(UINT instanceCounter, std::string metadata);
    what will be in the metadata is subject to change; i have yet to build a convention
-Rendering API is somewhat unsafe to use, be careful of memory leaks and/or resource exhausion!
-Try not to crash your program, although we have handlers to encounter some amount of crash such as access violation where we terminate your program, its still nitpicky to recover from fatal crashes, if you have managed to crash the framework
-If you need something to use that is not there yet, modify the framework to satisfy your needs and anything not hacky or bad will be accepted
