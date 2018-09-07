# XHybird
XHybird android Hybird 开发实践


## url重定向

## 返回时空白页

            if (!CommonUtils.isNull(response.getBuyurl())) {

                url = response.getBuyUrl();
                updateUrl(url, 1);
                webView.loadUrl(url);

                RxBus.getDefault().subscribeSticky(this, QuantManager.MOBILE_LOGIN, new RxBus.Callback<String>() {
                    @Override
                    public void onEvent(String s) {
                        webView.loadUrl("javascript:invalidVerifyCode(" + "" + ")");
                        RxBus.getDefault().removeStickyEvent(QuantManager.MOBILE_LOGIN, String.class);
                    }
                });
            }



    @Override
    public boolean onKeyDown(int keyCode, KeyEvent event) {
        if (KeyEvent.KEYCODE_BACK == keyCode) {
            titleBackBtn.performClick();
            return true;
        }
        return super.onKeyDown(keyCode, event);
    }

