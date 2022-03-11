#HOMEWORK

###Bài 1:

const obj1 = { x: 20, y: 30 };
function cloneDeep(obj) {
return {...obj}
};
const obj2 = cloneDeep(obj1)
obj2.x = 10

console.log(obj1)
console.log(obj2)

###Bài 2:

*Kết quả là:
macbooks = ['macbook2015', { model: 'm1' }, 'macbook2017']
apples = ['air', { model: 'm1' }, 'macbook2017']

*Giải thích
apples = macbooks sau khi được Spread Operator. Thế nhưng macbooks[1] là object vậy nên chỉ được lưu dưới giá
trị là tham chiếu địa chỉ ô nhớ vậy nên apples[1] và macbooks[1] đều cùng trỏ vào 1 vùng nhớ nên khi apples[1] modify 
giá trị của {model:'macbook2014'} = {model:'m1'} thì macbooks[1] cũng bị thay đổi theo. Còn macbooks[0] và macbook[2]
được lưu bởi 1 ô nhớ xác định nên khi apples copy giá trị thì ko thể làm thay đổi giá trị của string này.


###Bài 3:

var text = 'outside';
function show() {
  console.log(text) //1
  var text = 'inside';
}
const a = show();

*Kết quả là: undefined
*Giải thích: 
Với cơ chế hoisting js sẽ chuyển var text lên đầu trong function bên ngoài fuction text = 'outside'
nhưng trong hàm biến text bị var text ghi đè vậy nên kết quả console.log(text) sẽ trả về với giá trị 
là undefined
