# Flowchain Network Specs and Protocols 

## 1. P2P Network

### The Chord protocol

```
enum Chord_Protocol {
    NOTIFY_STABILIZE: 0,
    NOTIFY_PREDECESSOR: 1,
    NOTIFY_SUCCESSOR: 2,
    NOTIFY_JOIN: 3,
    FIND_SUCCESSOR: 4,
    FOUND_SUCCESSOR: 5,
    CHECK_PREDECESSOR: 6,
    CHECK_SUCESSOR: 7,
    CHECK_TTL: 8,
    MESSAGE: 9
};
```

### The Chord Message

```
struct chord_p2p_message {
    string nodeId;
    Chord_Protocol message;
    ipfs_data data;
};   
```

## 2. Virtual Blocks

### 

```
struct flowchain_chunk = {
    chord_p2p_message message;
};
```

### The IPFS hash

```
struct ipfs_data {
    string originFrom;
    string chordDataKey;
    string ipfsHash;
};
```
