#ui

```plantuml
abstract class SWidget {

}

class FSlotBase {
  -owner_ : const FChildren* 
  -widget_ : shared_ptr<SWidget>
}

class FChildren {

}

class SLeafWidget {

}

class SPanel {

}

class TSlotBase<T> {

}



SWidget <|-- SPanel
SWidget <|-- SLeafWidget

FSlotBase <|-- TSlotBase
```

