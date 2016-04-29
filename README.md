# MyDateTimePicker

//init
            DatePickerPopWin pickerPopWin = new DatePickerPopWin.Builder(MainActivity.this, new DatePickerPopWin.OnDatePickedListener() {
            @Override
            public void onDatePickCompleted(int year, int month, int day,int hour,int minute, String dateDesc) {
                        //TODO deal with dateDesc
                        Toast.makeText(MainActivity.this, dateDesc, Toast.LENGTH_SHORT).show();
                        }})
            .textConfirm("确定") //text of confirm button
            .textCancel("取消") //text of cancel button
            .btnTextSize(16) // button text size
            .viewTextSize(25) // pick view text size
            .colorCancel(Color.parseColor("#999999")) //color of cancel button
            .colorConfirm(Color.parseColor("#009900"))//color of confirm button
            .minYear(1990) //min year in loop
            .maxYear(2550) // max year in loop
            .dateChose("") // date chose when init popwindow
            .build();
//show             
        pickerPopWin.showPopWin(MainActivity.this);
