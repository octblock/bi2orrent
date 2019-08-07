# Aman
1.
```
int parse_bt_info(bt_info_t * bt_info, be_node * node);
```

2. 
```
/*choose a random id for this node*/
unsigned int select_id();
```

3. 
```
/*propogate a peer_t struct and add it to the bt_args structure*/
int add_peer(peer_t *peer, bt_args_t *bt_args, char * hostname, unsigned short port);
```

4. 
```
/*drop an unresponsive or failed peer from the bt_args*/
int drop_peer(peer_t *peer, bt_args_t *bt_args);
```

5. 
```
/* check status on peers, maybe they went offline? */
int check_peer(peer_t *peer);
```

6. 
```
/*check if peers want to send me something*/
int poll_peers(bt_args_t *bt_args);
```

7. 
```
/*send a msg to a peer*/
int send_to_peer(peer_t * peer, bt_msg_t * msg);
```
# brj
1. 
```
/*read a msg from a peer and store it in msg*/
int read_from_peer(peer_t * peer, bt_msg_t *msg);
```


2. 
```
/* save a piece of the file */
int save_piece(bt_args_t * bt_args, bt_piece_t * piece);
```

3. 
```
/*load a piece of the file into piece */
int load_piece(bt_args_t * bt_args, bt_piece_t * piece);
```

4. 
```
/*load the bitfield into bitfield*/
int get_bitfield(bt_args_t * bt_args, bt_bitfield_t * bitfield);
```

5. 
```
/*compute the sha1sum for a piece, store result in hash*/
int sha1_piece(bt_args_t * bt_args, bt_piece_t * piece, unsigned char * hash);
```


6. 
```
/*Contact the tracker and update bt_args with info learned, 
  such as peer list*/
int contact_tracker(bt_args_t * bt_args);
```

7. `bt_client.c`
