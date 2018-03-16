# Make File Tips

----------

##Android编译"missing separator"错误的解决
> Android.mk
> 
> include $(CLEAR_VARS)
> LOCAL_MODULE := KKBOX
> 
> ifeq ($(LC_PRODUCT_NAME), HTC_Asia_OC)
> 
>   ifeq ($(LCT_BUILD_TYPE), NORMAL)
>   
>     $(shell mkdir -p $(TARGET_OUT)/vendor/operator/app/KKBOX)
>     
>     $(shell cp -f $(LOCAL_PATH)/KKBOX.apk $(TARGET_OUT)/vendor/operator/app/KKBOX)
>     
>   endif 
>   
> endif 

#### 如果在最后的`endif`中未追加一个空格,就会报`missing separator`的错误,并停止编译;加上就可以了