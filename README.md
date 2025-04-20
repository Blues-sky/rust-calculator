# rust-calculator
First

use std::io;
fn main(){
  let mut a=String::new();
  let mut b=String::new();
  let mut o=String::new();
  println!();
  eprint!("Enter the first number:");
  io::stdin().read_line(&mut a).expect("msg");
  let a=a.trim().parse::<i32>().unwrap();
  eprint!("Enter the second number:");
  io::stdin().read_line(&mut b).expect("error");
  let b=b.trim().parse::<i32>().unwrap();
  eprint!("Enter the operator:");
  io::stdin().read_line(&mut o).expect("error");
  let o=o.trim().parse::<char>().unwrap();
  println!("calculated value is:{}",cal(a,b,o));
}
fn cal(a:i32,b:i32,o:char)->i32{
  match o{
    '+'=>a+b,
    '-'=>a-b,
    '*'=>a*b,
    '/'=>a/b,  
    _=>-1,
  }
}
