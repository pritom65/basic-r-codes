# basic-r-codes
names(radata)=radata %>% names() %>% tolower()
names(radata)=str_replace(names(radata),' ','_')

radata %>% map_df(class) %>% t() %>% format() %>% cbind(index=1:nrow(.))
names(radata)[16]='cordinates'
