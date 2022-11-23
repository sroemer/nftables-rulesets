# nftables-rulesets

## rulesets in this repository

basic: simple ruleset which only allows incoming ssh connections on port 22



## using a ruleset

Before activation of a ruleset the nftables service already should be running
because this service takes care of saving the active ruleset on shutdown
and reloading it on startup. A ruleset then can be loaded with `nft -f <file>`

On Gentoo and Artix linux with OpenRC run:

```
rc-update add nftables default  
rc-service nftables start  
nft -f nftables.conf  
```



## list currently active ruleset

For listing the currently active ruleset run:

```
nft list ruleset
```
