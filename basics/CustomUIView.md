# CustomUIView

making custom UIView 

```
 let topView:UIView = {
   	let view = UIView()
    view.translatesAutoresizingMaskIntoConstraints = false
    view.backgroundColor = #colorLiteral(red: 0.9803894353, green: 0.9803894353, blue: 0.9803894353, alpha: 1)
    return view
 }()
```

and set it in

```
 override init(frame:CGRect) {
   super.init(frame: frame)
   self.view.addSubview(topView)
}
```

constraints 

```
 fileprivate func setupContentViewConstraints() {
    contentView.translatesAutoresizingMaskIntoConstraints = false
    contentView.leftAnchor.constraint(equalTo: self.leftAnchor, constant: 10).isActive = true
    contentView.topAnchor.constraint(equalTo: self.safeAreaLayoutGuide.topAnchor, constant: 10).isActive = true
    contentView.rightAnchor.constraint(equalTo: self.rightAnchor, constant: -10).isActive = true
    contentView.bottomAnchor.constraint(equalTo: self.centerYAnchor, constant: 0).isActive = true
 }
```