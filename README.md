Unity-GUITips
=============

Various tips and resources for Unity3D GUI coding.



Property Drawer
---------------

### Usefult resources on github

* [property-drawer-collection](https://github.com/anchan828/property-drawer-collection) on github.
* [Tooltip Property Drawer](http://forum.unity3d.com/threads/211461-Tooltips-Property-Drawer) on Unity's forum.
* [Popup and IntRange property drawer](http://forum.unity3d.com/threads/150337-PropertyDrawers-for-easy-Inspector-customization/page2) on Unity's forum.


### Tutorials

* [자신 만의 PropertyDrawer를 만들자!](http://qiita.com/kyusyukeigo/items/8be4cdef97496a68a39d)
* [Making Unity Work for You](http://angrytroglodyte.net/home/index.php/how-we-do-it/tech-blog/75-making-unity-work-for-you)
* [Custom Data, an introduction to serialized classes and property drawers](http://catlikecoding.com/unity/tutorials/editor/custom-data/)
* [Custom List, displaying data your way](http://catlikecoding.com/unity/tutorials/editor/custom-list/)

* [Non trivial Property Drawers in Unity](http://gamenotgame.blogspot.kr/2013/12/non-trivial-property-drawers-in-unity.html)



Drag and Drop in the Editor
---------------------------

* [Drag and Drop in the editor - Explanation](http://forum.unity3d.com/threads/223242-Drag-and-Drop-in-the-editor-Explanation)


Custom Editor Plugins
---------------------

* [Reorderable List Editor Field for Unity](https://bitbucket.org/rotorz/reorderable-list-editor-field-for-unity) - List control for Unity allowing editor developers to add reorderable list controls to their GUIs.




Tips
----


* [유니티 게임 개발 소품, 쿨타임이 있는 쿨다운 스킬 버튼 만들기](http://hompy.info/660)
* [Creating a Circular Progressbar / Timer](http://answers.unity3d.com/questions/14770/creating-a-circular-progressbar-timer.html)


### A generic class for UnityEditor.Editor class

With deriving the given class for any Editor derived class, no need to type-casting of run-time type.

	public class InspectorBase<T> : Editor where T : UnityEngine.Object
	{
	   protected T Target { get { return (T) target; } }
	}


Usage:

	[CustomEditror(typeof(MyClass))]
	public class MyClassInspector : InspectorBase<MyClass>
	{
		public overrided void OnInspectorGUI()
		{

		}
	}
