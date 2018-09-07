# XHybird
XHybird android Hybird 开发实践


## url重定向

## 返回时空白页

    @Override
    public boolean onKeyDown(int keyCode, KeyEvent event) {
        if (KeyEvent.KEYCODE_BACK == keyCode) {
            titleBackBtn.performClick();
            return true;
        }
        return super.onKeyDown(keyCode, event);
    }

