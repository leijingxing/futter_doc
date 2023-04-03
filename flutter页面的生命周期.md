# flutter StatefulWidget的生命周期

### 1. StatefulWidget的生命周期
- StatefulWidget的生命周期分为三个阶段：**初始化阶段**、**运行阶段**、**销毁阶段**。

- 初始化阶段
    * 初始化阶段主要是StatefulWidget的初始化，包括StatefulWidget的创建、StatefulWidget的构建、StatefulWidget的渲染等。
    * StatefulWidget的创建主要是通过`StatefulWidget`类的`createState`方法来完成的。
    * StatefulWidget的构建主要是通过`StatefulWidget`类的`build`方法来完成的。
    * StatefulWidget的渲染主要是通过`StatefulWidget`类的`build`方法来完成的。

- 运行阶段
    * 运行阶段主要是StatefulWidget的运行，包括StatefulWidget的状态更新、StatefulWidget的状态改变、StatefulWidget的状态重建等。
    * StatefulWidget的状态更新主要是通过`StatefulWidget`类的`setState`方法来完成的。
    * StatefulWidget的状态改变主要是通过`StatefulWidget`类的`didChangeDependencies`方法来完成的。
    * StatefulWidget的状态重建主要是通过`StatefulWidget`类的`didUpdateWidget`方法来完成的。

- 销毁阶段
    * 销毁阶段主要是StatefulWidget的销毁，包括StatefulWidget的销毁、StatefulWidget的销毁等。
    * StatefulWidget的销毁主要是通过`StatefulWidget`类的`dispose`方法来完成的。

