# Master C# and Visual Studio Tricks & Shortcuts from A to Z

## Table of Contents
1. [Introduction to Productivity in Visual Studio](#1-introduction-to-productivity-in-visual-studio)
2. [Essential Keyboard Shortcuts](#2-essential-keyboard-shortcuts)
3. [Code Editor Tricks](#3-code-editor-tricks)
4. [Navigation Shortcuts](#4-navigation-shortcuts)
5. [Selection and Editing Tricks](#5-selection-and-editing-tricks)
6. [Code Snippets and Templates](#6-code-snippets-and-templates)
7. [IntelliSense Mastery](#7-intellisense-mastery)
8. [Refactoring Shortcuts](#8-refactoring-shortcuts)
9. [Debugging Tricks and Shortcuts](#9-debugging-tricks-and-shortcuts)
10. [Breakpoint Techniques](#10-breakpoint-techniques)
11. [Watch and Immediate Windows](#11-watch-and-immediate-windows)
12. [Solution Explorer Tricks](#12-solution-explorer-tricks)
13. [Find and Replace Mastery](#13-find-and-replace-mastery)
14. [Bookmarks and Navigation Aids](#14-bookmarks-and-navigation-aids)
15. [Code Cleanup and Formatting](#15-code-cleanup-and-formatting)
16. [Live Templates and Code Generation](#16-live-templates-and-code-generation)
17. [File and Window Management](#17-file-and-window-management)
18. [Git and Source Control Shortcuts](#18-git-and-source-control-shortcuts)
19. [Testing Shortcuts and Tricks](#19-testing-shortcuts-and-tricks)
20. [Performance Profiler Tips](#20-performance-profiler-tips)
21. [Extension Recommendations](#21-extension-recommendations)
22. [C# Language Tricks](#22-c-language-tricks)
23. [C# Modern Features Shortcuts](#23-c-modern-features-shortcuts)
24. [LINQ and Collection Tricks](#24-linq-and-collection-tricks)
25. [Async/Await Debugging Tricks](#25-asyncawait-debugging-tricks)
26. [Error List and Output Window](#26-error-list-and-output-window)
27. [Customization and Options](#27-customization-and-options)
28. [Productivity Power Tools](#28-productivity-power-tools)
29. [Cross-Platform Development Tips](#29-cross-platform-development-tips)
30. [Expert-Level Shortcuts](#30-expert-level-shortcuts)

---

## 1. Introduction to Productivity in Visual Studio

Visual Studio is one of the most powerful integrated development environments (IDEs) available, packed with features designed to maximize developer productivity. However, many developers only scratch the surface of what Visual Studio can do, missing out on features that could save them hours of work every week. This guide aims to unlock the full potential of Visual Studio and C# by revealing the tricks, shortcuts, and techniques that separate efficient developers from the rest.

The difference between a developer who knows Visual Studio well and one who doesn't is dramatic. A skilled Visual Studio user can navigate a massive codebase in seconds, refactor code safely with a few keystrokes, debug complex issues efficiently, and write code faster using snippets and IntelliSense effectively. These skills compound over time—a few seconds saved per operation adds up to hours over weeks and days over years. More importantly, these techniques reduce cognitive load, letting you focus on solving problems rather than fighting with your tools.

### Productivity Philosophy

```markdown
Productivity Principle #1: Keep your hands on the keyboard
- Mouse usage breaks your flow
- Every mouse action has a keyboard equivalent
- Learn shortcuts incrementally - one per day

Productivity Principle #2: Master the basics first
- Navigation (Go To, Find)
- Editing (Cut, Copy, Paste, Undo)
- Debugging (Step Over, Step Into, Continue)

Productivity Principle #3: Customize for your workflow
- Set up your ideal layout
- Install essential extensions
- Create custom snippets
```

### Visual Studio Edition Comparison

| Feature | Community | Professional | Enterprise |
|---------|-----------|--------------|------------|
| Core IDE | ✓ | ✓ | ✓ |
| CodeLens | Limited | ✓ | ✓ |
| Live Unit Testing | - | - | ✓ |
| IntelliTrace | - | - | ✓ |
| Code Clone | - | - | ✓ |
| Architecture Validation | - | - | ✓ |
| Code Map | - | - | ✓ |

### Setting Up for Success

```
First-time setup recommendations:
1. Sign in with Microsoft account to sync settings across machines
2. Choose your color theme (Tools → Options → Environment → General)
3. Set font size for readability (Tools → Options → Environment → Fonts and Colors)
4. Configure tab settings (Tools → Options → Text Editor → C# → Tabs)
5. Enable "Track Active Item in Solution Explorer"
6. Set up your default project location
```

---

## 2. Essential Keyboard Shortcuts

Mastering keyboard shortcuts is the single most impactful productivity improvement you can make. The time savings compound with every keystroke, and staying in "flow state" becomes much easier when you're not constantly reaching for the mouse. This section covers the absolute essential shortcuts that every developer should know, regardless of experience level.

The shortcuts in this guide use the default Visual Studio keybindings. If you've changed your scheme (like using ReSharper or VS Code keybindings), you may need to adapt these. You can always view your current keybindings in Tools → Options → Environment → Keyboard.

### The Absolute Essentials

| Action | Shortcut | Description |
|--------|----------|-------------|
| **Save** | `Ctrl + S` | Save current file |
| **Save All** | `Ctrl + Shift + S` | Save all open files |
| **Undo** | `Ctrl + Z` | Undo last action |
| **Redo** | `Ctrl + Y` | Redo last undone action |
| **Cut** | `Ctrl + X` | Cut selection (or line if no selection) |
| **Copy** | `Ctrl + C` | Copy selection (or line if no selection) |
| **Paste** | `Ctrl + V` | Paste from clipboard |
| **Select All** | `Ctrl + A` | Select everything in current document |
| **Find** | `Ctrl + F` | Find in current document |
| **Replace** | `Ctrl + H` | Find and replace in current document |
| **Find in Files** | `Ctrl + Shift + F` | Search across entire solution |

### Navigation Essentials

```csharp
// Most used navigation shortcuts

// Ctrl + K, Ctrl + D = Format entire document
// Ctrl + K, Ctrl + F = Format selection

// F12 = Go To Definition (most important shortcut!)
// Shift + F12 = Find All References
// Ctrl + - = Navigate Backward
// Ctrl + Shift + - = Navigate Forward
// Ctrl + M, Ctrl + M = Toggle Outlining (collapse/expand)
// Ctrl + M, Ctrl + O = Collapse to Definitions
// Ctrl + M, Ctrl + P = Stop Outlining

public class ExampleClass
{
    public void Method1()
    {
        // Place cursor on "Method2" and press F12
        Method2();
    }
    
    private void Method2()
    {
        // Press Ctrl + - to go back to Method1
    }
}
```

### Quick Launch

```
Quick Launch (Ctrl + Q) - Your command center
----------------------------------------------
Type anything to search menus, options, commands, and files

Examples:
• "font" → Opens font settings
• "dark" → Changes theme
• "git" → Shows Git commands
• "snippet" → Opens snippet manager
• "options" → Opens options dialog
• "new project" → Creates new project
```

### File Tab Management

| Action | Shortcut | Description |
|--------|----------|-------------|
| **Close Tab** | `Ctrl + F4` | Close current file |
| **Close All But This** | `Ctrl + Alt + F4` | Keep only current file open |
| **Next Tab** | `Ctrl + Tab` | Switch to next open file |
| **Previous Tab** | `Ctrl + Shift + Tab` | Switch to previous file |
| **Open File** | `Ctrl + O` | Open file dialog |
| **Recent Files** | `Ctrl + 1, Ctrl + R` | Show recent files |
| **Pin Tab** | Right-click tab | Keep tab open |

### Build and Run

```
Build Shortcuts
---------------
F5              = Start Debugging
Ctrl + F5       = Start Without Debugging
Ctrl + Shift + B = Build Solution
Ctrl + Break    = Cancel Build
F6              = Build Current Project (customizable)

Debug Shortcuts
---------------
F9              = Toggle Breakpoint
Ctrl + Shift + F9 = Delete All Breakpoints
F5              = Continue
Shift + F5      = Stop Debugging
F10             = Step Over
F11             = Step Into
Shift + F11     = Step Out
Ctrl + F10      = Run to Cursor
```

### Code Window Shortcuts

```csharp
// Essential editing shortcuts every developer needs

public class EditingExamples
{
    // Ctrl + K, Ctrl + C = Comment selection
    // Ctrl + K, Ctrl + U = Uncomment selection
    
    /* Select multiple lines and use comment shortcuts:
    Line one
    Line two
    Line three
    */
    
    public void Example()
    {
        // Ctrl + Delete = Delete word to the right
        // Ctrl + Backspace = Delete word to the left
        
        string text = "Hello World";
        
        // Ctrl + Left/Right Arrow = Move by word
        // Home = Go to line start
        // End = Go to line end
        
        // Ctrl + Home = Go to file start
        // Ctrl + End = Go to file end
    }
}
```

---

## 3. Code Editor Tricks

The code editor is where you spend most of your time, and Visual Studio offers numerous features to make coding faster and more enjoyable. From multi-line editing to smart indenting, these tricks will transform how you write code. Understanding these features helps you write cleaner code faster and with fewer keystrokes.

### Multi-Line and Block Selection

```csharp
// ALT + Mouse Drag = Box/Block Selection
// ALT + SHIFT + Arrow Keys = Box Selection with keyboard

// Example: Edit multiple lines at once
// Before block selection:
public int    GetId()    => id;
public string GetName()  => name;
public int    GetAge()   => age;

// Use block selection to change all return types at once
// Before block selection:
public string GetId()    => id;
public string GetName()  => name;
public string GetAge()   => age;

// Zero-width box selection (ALT + Click)
// Insert same text on multiple lines:
public void Method1();
public void Method2();
public void Method3();
// Place zero-width box at start and type "async "
// Result:
async public void Method1();
async public void Method2();
async public void Method3();
```

### Line Manipulation

```csharp
public class LineManipulation
{
    // Ctrl + Enter = Insert blank line above (current line moves down)
    // Ctrl + Shift + Enter = Insert blank line below
    
    // Shift + Alt + Up/Down Arrow = Duplicate line
    // Alt + Up/Down Arrow = Move line up/down
    
    public void Example()
    {
        // Type this line, then press Ctrl+Enter
        // Cursor creates new line above, this line moves down
        
        // Duplicate this line with Shift+Alt+Down
        // Duplicate this line with Shift+Alt+Down
        
        // Move this line up/down with Alt+Up/Down
    }
    
    // Ctrl + L = Delete entire line (cut to clipboard)
    // Ctrl + Shift + L = Delete entire line (no clipboard)
    // Shift + Delete = Same as Ctrl + L
}
```

### Word and Selection Tricks

```csharp
public class SelectionTricks
{
    public void Example()
    {
        // Ctrl + W = Select word (press multiple times to expand)
        string variableName = "value";
        // First Ctrl+W: selects "variableName"
        // Second Ctrl+W: selects entire statement
        
        // Shift + Home = Select to line start
        // Shift + End = Select to line end
        // Ctrl + Shift + Home = Select to file start
        // Ctrl + Shift + End = Select to file end
        
        // Ctrl + Shift + ] = Select to matching brace
        if (true)
        {
            // Cursor on "if" brace, selects entire block
        }
        
        // Triple-click = Select entire line
        // Ctrl + Click (on symbol) = Navigate to definition
    }
}
```

### Smart Indentation and Formatting

```csharp
// Auto-format shortcuts:

// Ctrl + K, Ctrl + D = Format entire document
// Ctrl + K, Ctrl + F = Format selection

// Format on paste (automatic) - configurable in Options

public class Formatting
{
    public void PoorlyFormatted(){
    int x=1;
    string y="test";
    if(x==1){y="changed";}
    }
    
    // After Ctrl+K, Ctrl+D:
    public void WellFormatted()
    {
        int x = 1;
        string y = "test";
        if (x == 1) { y = "changed"; }
    }
}
```

### Code Cleanup (Visual Studio 2019+)

```
Code Cleanup (Ctrl + K, Ctrl + E)
----------------------------------
Runs multiple fixes at once:
• Fix code style
• Sort usings
• Remove unnecessary usings
• Apply implicit/explicit type preferences
• Add missing accessibility modifiers
• And more (configurable)

Configure in: Tools → Options → Text Editor → C# → Code Style → Formatting
```

### Vertical Scroll Bar Map

```
Enable the scroll bar map to see code overview:
1. Right-click scroll bar → Scroll Bar Options
2. Select "Use map mode for vertical scroll bar"
3. Adjust width and preview behavior

Benefits:
• See entire file at a glance
• Click to navigate instantly
• Shows breakpoints, errors, search results
• Hover for code preview
```

---

## 4. Navigation Shortcuts

Efficient navigation is the hallmark of an experienced Visual Studio user. Being able to move through a large codebase quickly, find what you're looking for, and understand code relationships saves enormous amounts of time. These navigation shortcuts work across files, projects, and even across your entire solution.

### Go To Commands

```
Navigate To (Ctrl + , or Ctrl + T)
-----------------------------------
The most powerful navigation command
Search for files, types, members, symbols

Examples:
• "HomeController" → Jump to controller
• "GetById" → Jump to method
• "Product.cs" → Jump to file
• "IPayment" → Jump to interface
• "f:Product" → Search only files
• "t:Product" → Search only types
• "m:GetById" → Search only members
```

### Go To Definition and References

```csharp
public class NavigationExample
{
    public void ProcessOrder(Order order)
    {
        // F12 = Go To Definition
        // Place cursor on "Order" and press F12
        
        // Ctrl + F12 = Go To Declaration (for partial classes)
        
        // Shift + F12 = Find All References
        // Shows everywhere "Order" is used
        
        // Alt + F12 = Peek Definition (preview without navigating)
        // Opens inline window showing definition
        
        // K + R (Ctrl + K, R) = Find All References (alternate)
        
        var result = order.CalculateTotal();
        // F12 on CalculateTotal → jumps to method
        // Alt + F12 → shows method inline
    }
}

// Peek Definition allows browsing within peek window:
// Use Tab to navigate between references
// Esc to close peek window
// F12 inside peek window to go to full definition
```

### Navigate Backward and Forward

```
Navigate Through History
------------------------
Ctrl + - (minus) = Navigate Backward
Ctrl + Shift + - (minus) = Navigate Forward

These track your cursor movement history
Essential when exploring unfamiliar code

Workflow example:
1. Start at HomeController
2. F12 on Order class
3. F12 on CalculateTotal method
4. Ctrl + - = Back to Order class
5. Ctrl + - = Back to HomeController
6. Ctrl + Shift + - = Forward to Order class
```

### File and Type Navigation

```
Go To File (Ctrl + 1, Ctrl + F or Ctrl + Shift + T)
----------------------------------------------------
Quick file search with fuzzy matching
Type "hmc" → finds "HomeController.cs"

Go To Type (Ctrl + 1, Ctrl + T)
-------------------------------
Navigate directly to type definition

Go To Member (Ctrl + 1, Ctrl + M)
---------------------------------
Search within current file for members
Type "get" → finds GetById, GetAll, etc.

Go To Symbol (Ctrl + 1, Ctrl + S)
---------------------------------
Search for symbols across solution

Go To Line (Ctrl + G)
---------------------
Jump to specific line number
Useful for debugging error messages
```

### Solution Explorer Navigation

```
Solution Explorer Tricks
------------------------
Ctrl + ; = Search in Solution Explorer
          (finds files, folders, types)

Ctrl + [ , S = Sync with Active Document
          (highlights current file in Solution Explorer)

Right-click file → Scope to This
          (shows only this file's project)

Shift + Alt + Enter = Full Screen Mode
          (maximizes editor, hides other windows)

F4 = Properties Window
Shift + F4 = Properties Pages (project settings)
```

### Type Hierarchy Navigation

```csharp
// Navigate inheritance hierarchies

// Ctrl + K, Ctrl + O = Go To Base Type
// Place cursor on derived class, jumps to base

// Ctrl + K, Ctrl + R = Find All Derived Types
// Shows all classes that inherit from this

// Ctrl + M, Ctrl + O = Collapse to Definitions
// Useful for overview of large files

public class BaseClass { }
public class DerivedClass : BaseClass { }
// On "DerivedClass", Ctrl+K, Ctrl+O → jumps to BaseClass
// On "BaseClass", Ctrl+K, Ctrl+R → shows DerivedClass

// View Class Diagram (Project context menu)
// Visual representation of class hierarchy
```

---

## 5. Selection and Editing Tricks

Advanced selection and editing techniques allow you to manipulate code with precision and speed. These tricks go beyond simple copy and paste, enabling you to select complex code blocks, swap elements, and edit multiple locations simultaneously.

### Incremental Selection

```csharp
public class IncrementalSelection
{
    public void Example()
    {
        // Ctrl + W = Expand selection
        // Ctrl + Shift + W = Shrink selection
        
        string message = "Hello World";
        
        // Start with cursor on "message"
        // Press Ctrl+W repeatedly:
        // 1. Selects "message"
        // 2. Selects "message = "Hello World""
        // 3. Selects entire statement with semicolon
        // 4. Selects entire block
        // 5. Selects entire method
        // 6. Selects entire class
    }
}
```

### Block Editing

```csharp
public class BlockEditing
{
    // Scenario: Convert fields to properties
    
    // Original fields:
    private int id;
    private string name;
    private decimal price;
    
    // ALT + Mouse drag to select "private "
    // Type "public " - replaces all at once
    
    // Result:
    public int id;
    public string name;
    public decimal price;
    
    // ALT + Mouse drag to select "id;", "name;", "price;"
    // Delete and type "Id { get; set; }"
    // But this works poorly for different lengths...
    
    // Better: Multi-cursor via multiple carets
    // In VS 2022: Ctrl + Alt + Click for multiple carets
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
}
```

### Parameter Manipulation

```csharp
public class ParameterTricks
{
    // Ctrl + . on parameter → shows refactoring options
    // • Rename parameter
    // • Add null check
    // • Introduce parameter
    
    public void Process(string name, int count, bool isActive)
    {
        // Ctrl + Shift + Up/Down = Swap parameters
        // (requires Productivity Power Tools or similar)
        
        // Use Ctrl + . for:
        // • Reorder parameters
        // • Remove parameter
        // • Add parameter
    }
    
    // After reordering:
    public void Process(int count, string name, bool isActive)
    {
        // Parameters swapped, all call sites updated
    }
}
```

### Code Transposition

```csharp
public class TranspositionExamples
{
    public void Example()
    {
        int a = 1, b = 2;
        
        // Want to swap values
        // Select both assignments, use:
        // Shift + Alt + T = Transpose (if available via extension)
        
        // Built-in: Move lines up/down with Alt + Up/Down
        // Move statement:
        int first = 1;
        int second = 2;
        // Alt+Up on "second" line:
        int second = 2;
        int first = 1;
    }
    
    public void ArrayExample()
    {
        var items = new[] { "a", "b", "c", "d" };
        
        // Ctrl + Delete = Delete word forward
        // Ctrl + Backspace = Delete word backward
        
        // Triple-click line → selects entire line
        // Drag selection → moves text
    }
}
```

### Clipboard Ring

```
Clipboard Ring (Ctrl + Shift + V)
---------------------------------
Visual Studio keeps history of copied items
Cycle through past clipboard contents

Workflow:
1. Copy "First text" (Ctrl + C)
2. Copy "Second text" (Ctrl + C)
3. Copy "Third text" (Ctrl + C)
4. Paste (Ctrl + V) → "Third text"
5. Ctrl + Shift + V → "Second text"
6. Ctrl + Shift + V again → "First text"
7. Press Enter to select

Useful for:
• Pasting multiple values repeatedly
• Recovering previously copied code
• Template insertion
```

---

## 6. Code Snippets and Templates

Code snippets are pre-written code templates that you can insert quickly using short abbreviations. Visual Studio includes many built-in snippets for common patterns, and you can create your own for frequently used code. Snippets dramatically speed up coding by reducing typing and ensuring consistency.

### Built-in Code Snippets

```csharp
// HOW TO USE SNIPPETS:
// 1. Type the snippet shortcut
// 2. Press Tab twice to insert
// 3. Fill in the highlighted placeholders
// 4. Press Tab to move between placeholders
// 5. Press Enter when done

// CLASSIC SNIPPETS:

// "cw" + Tab + Tab
Console.WriteLine();

// "for" + Tab + Tab
for (int i = 0; i < length; i++)
{

}

// "foreach" + Tab + Tab
foreach (var item in collection)
{

}

// "if" + Tab + Tab
if (true)
{

}

// "else" + Tab + Tab
else
{

}

// "try" + Tab + Tab
try
{

}
catch (Exception)
{

    throw;
}

// "tryf" + Tab + Tab
try
{

}
finally
{

}

// "prop" + Tab + Tab
public int MyProperty { get; set; }

// "propfull" + Tab + Tab
private int myVar;

public int MyProperty
{
    get { return myVar; }
    set { myVar = value; }
}

// "ctor" + Tab + Tab (constructor)
public ClassName()
{

}

// "sim" + Tab + Tab (static int Main)
static int Main(string[] args)
{
    return 0;
}

// "svm" + Tab + Tab (static void Main)
static void Main(string[] args)
{

}
```

### Surround-With Snippets

```csharp
// SURROUND-WITH SNIPPETS: Ctrl + K, Ctrl + S

// Select code, then press Ctrl + K, Ctrl + S

// Example 1: Surround with "if"
var value = GetValue();
// Select "var value = GetValue();"
// Ctrl + K, S → choose "if"
if (true)
{
    var value = GetValue();
}

// Example 2: Surround with "try"
SomeRiskyOperation();
// Select line, Ctrl + K, S → choose "try"
try
{
    SomeRiskyOperation();
}
catch (Exception)
{

    throw;
}

// Other surround-with snippets:
// #region / #endregion
// class
// do
// while
// lock
// using
```

### Creating Custom Snippets

```xml
<!-- Custom snippet file (.snippet) -->
<?xml version="1.0" encoding="utf-8"?>
<CodeSnippets xmlns="http://schemas.microsoft.com/VisualStudio/2005/CodeSnippet">
  <CodeSnippet Format="1.0.0">
    <Header>
      <Title>notify</Title>
      <Shortcut>notify</Shortcut>
      <Description>Property with INotifyPropertyChanged</Description>
      <Author>Your Name</Author>
    </Header>
    <Snippet>
      <Declarations>
        <Literal>
          <ID>type</ID>
          <Default>int</Default>
          <ToolTip>Property type</ToolTip>
        </Literal>
        <Literal>
          <ID>property</ID>
          <Default>MyProperty</Default>
          <ToolTip>Property name</ToolTip>
        </Literal>
        <Literal>
          <ID>field</ID>
          <Default>myProperty</Default>
          <ToolTip>Field name</ToolTip>
        </Literal>
      </Declarations>
      <Code Language="csharp">
        <![CDATA[private $type$ $field$;

public $type$ $property$
{
    get => $field$;
    set
    {
        if ($field$ != value)
        {
            $field$ = value;
            OnPropertyChanged(nameof($property$));
        }
    }
}$end$]]>
      </Code>
    </Snippet>
  </CodeSnippet>
</CodeSnippets>

<!-- Save as "notify.snippet" and import via:
     Tools → Code Snippets Manager → Import
-->
```

### File Templates

```csharp
// Visual Studio creates default file templates
// Customize templates for your team:

// Location (varies by VS version):
// C:\Program Files\Microsoft Visual Studio\2022\Enterprise\Common7\IDE\ItemTemplates\CSharp\Code\1033\Class

// Create custom templates:
// 1. Create template file with parameters
// 2. Add .vstemplate file
// 3. Zip together
// 4. Place in user templates folder

// Example Class.cs template:
using System;
using System.Collections.Generic;
$if$ ($targetframeworkversion$ >= 3.5)using System.Linq;
$endif$using System.Text;
$if$ ($targetframeworkversion$ >= 4.5)using System.Threading.Tasks;
$endif$

namespace $rootnamespace$
{
    public class $safeitemrootname$
    {
        // Created by: $username$
        // Created on: $time$
        
        public $safeitemrootname$()
        {
        }
    }
}

// Template Parameters:
// $safeitemname$ - sanitized file name
// $itemname$ - original file name
// $rootnamespace$ - project default namespace
// $username$ - Windows user name
// $time$ - current date/time
// $year$ - current year
```

### Snippet Manager

```
Tools → Code Snippets Manager (Ctrl + K, Ctrl + B)
---------------------------------------------------
• View all installed snippets
• Import custom snippets
• Search snippets
• View snippet code

Snippet locations:
• Built-in: C:\Program Files\...\VC#\Snippets\
• User: Documents\Visual Studio 2022\Code Snippets\
```

---

## 7. IntelliSense Mastery

IntelliSense is Visual Studio's code completion system that provides suggestions, parameter info, quick info, and more as you type. Mastering IntelliSense significantly speeds up coding by reducing typing, preventing errors, and providing quick access to documentation. Many developers underutilize IntelliSense, missing out on features that could make them more productive.

### IntelliSense Basics

```csharp
public class IntelliSenseBasics
{
    // BASIC COMPLETION
    // Type and IntelliSense suggests automatically
    // Ctrl + Space = Force show IntelliSense
    
    // TAB vs ENTER
    // Tab = Insert suggestion (stay in completion mode)
    // Enter = Insert suggestion (exit completion mode)
    
    // NAVIGATION
    // Up/Down arrows = Navigate suggestions
    // Page Up/Down = Jump by page in list
    
    // FILTERING
    // Type to filter the list
    // CamelCase filtering works: "GTI" finds "GetTotalItems"
    
    public void Example()
    {
        // Type "cw" then Tab twice for:
        Console.WriteLine();
        
        // Type "Guid.N" and IntelliSense shows:
        Guid.NewGuid();
        
        // Type parameters shows automatically
        // Method(parameter1, parameter2)
    }
}
```

### IntelliSense Modes

```
IntelliSense Completion Modes
-----------------------------

1. Standard Mode (default)
   - Shows all possible completions
   - Most flexible but larger list

2. Prediction Mode
   - Shows most likely completion first
   - Learns from your patterns

Toggle: Ctrl + Alt + Space
Or: Edit → IntelliSense → Toggle Completion Mode
```

### IntelliSense Icons

```
Understanding IntelliSense Icons
--------------------------------
📦 Namespace
📁 Folder
📄 File
🏛️ Class
📐 Struct
📋 Interface
📧 Delegate
⚡ Enum
🔷 Constant
🟢 Method
🔷 Property
🔵 Field
📄 Event
🔧 Extension Method
⬆️ Inherited Member
🔒 Private
🔓 Public
🔐 Protected
```

### Parameter Info

```csharp
public class ParameterInfo
{
    // Ctrl + Shift + Space = Show Parameter Info
    // Useful when parameter info disappears
    
    public void ProcessOrder(
        int orderId,           // Parameter info shows this
        string customerName,   // and this
        decimal amount,        // and this
        bool isPriority = false // including default values
    )
    {
        // Type "ProcessOrder(" to see parameter info
        // Press Up/Down arrows to see overloads
    }
    
    public void ProcessOrder(int orderId)
    {
        // Overload - Up/Down arrows show different signatures
    }
    
    public void Example()
    {
        // Type "ProcessOrder(" then Ctrl+Shift+Space
        ProcessOrder(1, "John", 100.00m, true);
    }
}
```

### Quick Info

```csharp
public class QuickInfo
{
    // Hover over symbol for Quick Info
    // Shows: Type, summary, parameters, returns
    
    /// <summary>
    /// Calculates the total order value including tax.
    /// </summary>
    /// <param name="subtotal">The order subtotal</param>
    /// <param name="taxRate">The tax rate as decimal (0.08 = 8%)</param>
    /// <returns>Total including tax</returns>
    public decimal CalculateTotal(decimal subtotal, decimal taxRate)
    {
        return subtotal * (1 + taxRate);
    }
    
    // Ctrl + K, Ctrl + I = Show Quick Info
    // (Works without mouse)
    
    public void Example()
    {
        // Place cursor on "CalculateTotal"
        // Press Ctrl+K, Ctrl+I to see documentation
        var total = CalculateTotal(100m, 0.08m);
    }
}
```

### IntelliSense Filtering

```csharp
public class IntelliSenseFiltering
{
    // FILTER BY MEMBER TYPE
    // Ctrl + J = Toggle showing all members
    
    // After typing "." on an object:
    // Icons at bottom filter by type:
    // 🟢 Methods only
    // 🔷 Properties only  
    // 🔵 Fields only
    // 📄 Events only
    
    // CAMELCASE FILTERING
    List<string> items = new List<string>();
    
    // Type "items.aetw"
    // Finds: items.AddEachToStringWith()
    
    // PASCAL CASE FILTERING  
    // "GTI" finds: GetTotalItems()
    
    // SNAKE_CASE works too
    // "get_total" finds: Get_Total_Value()
    
    // FUZZY MATCHING (VS 2022)
    // "gti" finds: GetTotalItems()
    // Even works with typos: "gtit" still finds it
}
```

### Code Completion Tricks

```csharp
public class CompletionTricks
{
    // AUTO-IMPORT ON COMPLETION
    // Type unrecognized class, Ctrl + . to import
    
    // Example: Type "HttpClient" (not imported)
    // Press Ctrl + . → imports System.Net.Http
    
    // TAB TO COMPLETE PROPERTY NAMES
    public int MyVeryLongPropertyName { get; set; }
    
    public void Example()
    {
        // Type "this.mvlp" + Tab
        // Expands to: this.MyVeryLongPropertyName
    }
    
    // CORRECTION ON THE FLY
    // Type "stringbuilder" (lowercase)
    // Ctrl + . → corrects to "StringBuilder"
    
    // GENERATE FROM USAGE
    // Type method that doesn't exist:
    public void NewFeature()
    {
        // CallNewMethod() doesn't exist
        // Ctrl + . → Generate method
    }
}
```

---

## 8. Refactoring Shortcuts

Refactoring is the process of restructuring existing code without changing its external behavior. Visual Studio provides powerful refactoring tools that safely transform your code while maintaining correctness. These refactorings save time and reduce errors compared to manual code changes.

### Quick Actions (Ctrl + .)

```csharp
// Ctrl + . (or Alt + Enter) = Quick Actions menu
// The most important refactoring shortcut

public class QuickActions
{
    private string name;
    
    public void Example()
    {
        // GENERATE MEMBERS
        // Type property that doesn't exist:
        this.NewProperty = "test"; // Ctrl + . → Generate property
        
        // ADD MISSING USING
        // Type unimported class:
        // HttpClient client; // Ctrl + . → Import namespace
        
        // FIX CODE ISSUES
        // Unused variable:
        int unused = 5; // Ctrl + . → Remove unused variable
        
        // IMPLEMENT INTERFACE
        // : IComparable // Ctrl + . → Implement interface
    }
    
    // CONVERT BETWEEN LOOP TYPES
    // Place cursor on loop, Ctrl + .
    
    public void LoopConversion()
    {
        var items = new List<int> { 1, 2, 3 };
        
        // for → foreach conversion
        for (int i = 0; i < items.Count; i++)
        {
            Console.WriteLine(items[i]);
        }
        
        // foreach → for conversion
        foreach (var item in items)
        {
            Console.WriteLine(item);
        }
        
        // for/foreach → LINQ
        // Ctrl + . → Convert to LINQ
    }
}
```

### Rename Refactoring

```csharp
// F2 or Ctrl + R, Ctrl + R = Rename
// Safely renames across entire solution

public class RenameExample
{
    // Original name
    private int _count;
    
    public int Count
    {
        get => _count;
        set => _count = value;
    }
    
    public void IncrementCount()
    {
        _count++;
    }
    
    // Place cursor on "_count" and press F2
    // Type new name: "_totalCount"
    // ALL references update automatically:
    
    private int _totalCount;
    
    public int TotalCount
    {
        get => _totalCount;
        set => _totalCount = value;
    }
    
    public void IncrementTotalCount()
    {
        _totalCount++;
    }
}
```

### Extract Method

```csharp
public class ExtractMethodExample
{
    public void ProcessOrder(Order order)
    {
        // Select code to extract:
        decimal subtotal = 0;
        foreach (var item in order.Items)
        {
            subtotal += item.Price * item.Quantity;
        }
        decimal tax = subtotal * 0.08m;
        decimal total = subtotal + tax;
        
        // Ctrl + R, Ctrl + M = Extract Method
        // Named: CalculateOrderTotal
        
        // After extraction:
        decimal total = CalculateOrderTotal(order);
    }
    
    // Generated method:
    private decimal CalculateOrderTotal(Order order)
    {
        decimal subtotal = 0;
        foreach (var item in order.Items)
        {
            subtotal += item.Price * item.Quantity;
        }
        decimal tax = subtotal * 0.08m;
        decimal total = subtotal + tax;
        return total;
    }
}
```

### Extract Interface

```csharp
// Ctrl + R, Ctrl + I = Extract Interface

public class CustomerRepository
{
    public Customer GetById(int id) => throw new NotImplementedException();
    public List<Customer> GetAll() => throw new NotImplementedException();
    public void Add(Customer customer) => throw new NotImplementedException();
    public void Update(Customer customer) => throw new NotImplementedException();
    public void Delete(int id) => throw new NotImplementedException();
}

// After extracting interface (Ctrl + R, Ctrl + I):
// Creates ICustomerRepository with selected members

public interface ICustomerRepository
{
    Customer GetById(int id);
    List<Customer> GetAll();
    void Add(Customer customer);
    void Update(Customer customer);
    void Delete(int id);
}

public class CustomerRepository : ICustomerRepository
{
    // Implementation remains
}
```

### Encapsulate Field

```csharp
// Ctrl + R, Ctrl + E = Encapsulate Field

public class Product
{
    // Before: public field
    public decimal price;
}

// After Ctrl + R, Ctrl + E on "price":
public class Product
{
    private decimal price;
    
    public decimal Price
    {
        get => price;
        set => price = value;
    }
}
```

### Other Essential Refactorings

```csharp
public class OtherRefactorings
{
    private string firstName;
    private string lastName;
    private string email;
    
    // EXTRACT CLASS
    // Select multiple fields, Ctrl + R, Ctrl + O
    // Moves fields to new class
    
    // EXTRACT LOCAL FUNCTION
    // Select code, Ctrl + R, Ctrl + M (inside method)
    
    // INLINE TEMPORARY VARIABLE
    // Ctrl + R, Ctrl + I on variable declaration
    
    // INTRODUCE PARAMETER
    // Ctrl + R, Ctrl + P on local variable
    
    // REORDER PARAMETERS
    // Ctrl + R, Ctrl + O on method signature
    
    // REMOVE PARAMETERS
    // Ctrl + R, Ctrl + V on method signature
    
    // CHANGE SIGNATURE
    // Ctrl + R, Ctrl + S (combined reordering, adding, removing)
    
    // MOVE TYPE TO MATCHING FILE
    // Ctrl + . on class name
    
    // PULL MEMBERS UP
    // Move members to base class
    
    // PUSH MEMBERS DOWN
    // Move members to derived class
}
```

### Refactoring Shortcuts Summary

| Shortcut | Action | Description |
|----------|--------|-------------|
| `F2` | Rename | Rename symbol across solution |
| `Ctrl + R, Ctrl + R` | Rename | (Alternative) |
| `Ctrl + R, Ctrl + M` | Extract Method | Create method from selection |
| `Ctrl + R, Ctrl + I` | Extract Interface | Create interface from class |
| `Ctrl + R, Ctrl + E` | Encapsulate Field | Create property from field |
| `Ctrl + R, Ctrl + V` | Remove Parameters | Remove method parameters |
| `Ctrl + R, Ctrl + O` | Reorder Parameters | Change parameter order |
| `Ctrl + R, Ctrl + S` | Change Signature | Comprehensive signature change |
| `Ctrl + .` | Quick Actions | Context-aware refactoring menu |
| `Ctrl + R, Ctrl + D` | Duplicate Line | Copy current line |

---

## 9. Debugging Tricks and Shortcuts

Debugging is where you spend significant time as a developer, and Visual Studio offers an extensive debugging toolkit. Mastering debugging shortcuts and techniques helps you find bugs faster and understand code behavior better. From basic stepping to advanced breakpoint conditions, these features transform debugging from a frustrating experience into a powerful investigation tool.

### Basic Debugging Shortcuts

```
STARTING DEBUGGING
------------------
F5              = Start Debugging
Ctrl + F5       = Start Without Debugging
Shift + F5      = Stop Debugging
Ctrl + Shift + F5 = Restart Debugging

STEPPING
--------
F10             = Step Over (execute line, don't enter functions)
F11             = Step Into (enter function calls)
Shift + F11     = Step Out (exit current function)
Ctrl + F10      = Run to Cursor (execute until cursor position)

BREAKPOINTS
-----------
F9              = Toggle Breakpoint
Ctrl + F9       = Toggle Breakpoint Enabled
Ctrl + Shift + F9 = Delete All Breakpoints
```

### Debugging Windows

```csharp
// OPENING DEBUG WINDOWS (available during debugging)

// Ctrl + D, L = Locals Window
// Shows all local variables in current scope

// Ctrl + D, A = Autos Window  
// Shows variables used around current line

// Ctrl + Alt + W, 1 = Watch Window 1
// Add expressions to monitor

// Ctrl + D, I = Immediate Window
// Execute code, evaluate expressions

// Ctrl + D, C = Call Stack
// Shows method call hierarchy

// Ctrl + D, T = Threads Window
// View all threads in debugging session

public class DebuggingWindows
{
    public void Example()
    {
        var items = Enumerable.Range(1, 100).ToList();
        var filtered = items.Where(x => x % 2 == 0).ToList();
        var sum = filtered.Sum();
        
        // Set breakpoint here
        // View Locals to see: items, filtered, sum
        // Watch: filtered.Count, filtered.Average()
        // Immediate: items.Count, filtered.First()
    }
}
```

### DataTips

```csharp
public class DataTips
{
    public void ProcessOrder(Order order)
    {
        // Hover over variable during debugging
        // Shows value in tooltip (DataTip)
        
        // PINNED DATATIPS
        // Click pin icon to keep DataTip visible
        // Persists across debugging sessions
        // Add comments to pinned values
        
        var total = order.Items.Sum(i => i.Price * i.Quantity);
        
        // Expand DataTip to see object properties
        // Right-click for copy, add to watch
    }
    
    // DataTips can show:
    // • Object properties
    // • Collection contents
    // • Computed expressions (add custom)
    // • Raw view (without property getters)
}
```

### Edit and Continue

```csharp
// Edit and Continue allows code changes while debugging
// Applies changes without restarting

public class EditAndContinue
{
    public void Example(int value)
    {
        // Set breakpoint here
        int result = value * 2;
        
        // Hit breakpoint, pause execution
        // Change "2" to "3"
        // Continue (F5) - changes applied
        
        // Supported changes:
        // • Modify method bodies
        // • Add new methods
        // • Add new fields/properties
        // • Add new classes
        
        // NOT supported:
        // • Change method signatures
        // • Modify LINQ expressions
        // • Change generic types
    }
}
```

### Debugging Attributes

```csharp
using System.Diagnostics;

public class DebuggingAttributes
{
    // DebuggerDisplay - custom display in debugger
    [DebuggerDisplay("Order {Id} - {CustomerName} - ${Total}")]
    public class Order
    {
        public int Id { get; set; }
        public string CustomerName { get; set; }
        public decimal Total { get; set; }
    }
    
    // DebuggerBrowsable - hide from debugger
    public class SecureData
    {
        public string PublicInfo { get; set; }
        
        [DebuggerBrowsable(DebuggerBrowsableState.Never)]
        public string Password { get; set; }  // Hidden in debugger
        
        [DebuggerBrowsable(DebuggerBrowsableState.RootHidden)]
        public int[] Items = { 1, 2, 3 };  // Shows array items directly
    }
    
    // DebuggerStepThrough - skip when stepping
    [DebuggerStepThrough]
    public void Log(string message)
    {
        // Debugger won't step into this method
        Console.WriteLine(message);
    }
    
    // DebuggerHidden - hide from debugger entirely
    [DebuggerHidden]
    public void InternalHelper()
    {
        // Won't appear in call stack
    }
    
    // DebuggerNonUserCode - mark as non-user code
    [DebuggerNonUserCode]
    public void GeneratedCode()
    {
        // Treated as framework code
    }
}
```

### Debugging Lambda Expressions

```csharp
public class LambdaDebugging
{
    // VS 2022 can debug lambda expressions
    public void Example()
    {
        var numbers = Enumerable.Range(1, 10);
        
        // Set breakpoint on next line
        var result = numbers
            .Where(x => x % 2 == 0)    // Can step into
            .Select(x => x * x)         // Can step into
            .ToList();
        
        // In Immediate Window:
        // numbers.Where(x => x > 5).ToList()
        // numbers.Count(x => x % 2 == 0)
        
        // In Watch Window:
        // numbers.Where(x => x > 5)
        // result.Sum()
    }
}
```

### Exception Settings

```
Exception Settings (Ctrl + D, E)
--------------------------------
Control when debugger breaks on exceptions

• Common Language Runtime Exceptions
• C++ Exceptions
• Win32 Exceptions
• JavaScript Runtime Exceptions

Break when thrown:
☑ Common Language Runtime Exceptions
  ☐ System.NullReferenceException
  ☑ System.IndexOutOfRangeException
  
Break when unhandled (default):
☑ Common Language Runtime Exceptions
  ☑ All CLR exceptions

Add custom exception:
Right-click → Add Exception
Enter: MyCustomException
```

---

## 10. Breakpoint Techniques

Breakpoints are your primary tool for pausing program execution at specific points. Beyond simple line breakpoints, Visual Studio offers conditional breakpoints, hit count breakpoints, tracepoints, and more. Understanding these advanced breakpoint features helps you debug complex scenarios more efficiently.

### Basic Breakpoints

```csharp
public class BasicBreakpoints
{
    public void Example()
    {
        int x = 10;          // F9 = Toggle breakpoint
        int y = 20;          // Click margin to add
        int result = x + y;  // Red circle = enabled breakpoint
        
        // Ctrl + F9 = Disable/enable breakpoint
        // Disabled breakpoint = hollow circle
        
        // Right-click breakpoint → Delete
        // Ctrl + Shift + F9 = Delete all breakpoints
    }
}
```

### Conditional Breakpoints

```csharp
public class ConditionalBreakpoints
{
    public void ProcessItems(List<int> items)
    {
        foreach (var item in items) // 1000 iterations
        {
            // Don't want to break 1000 times!
            // Right-click breakpoint → Conditions
            
            // CONDITION EXAMPLES:
            // item == 500           // Break only when item is 500
            // item > 100 && item < 200
            // item % 100 == 0       // Every 100th item
            
            ProcessItem(item);
        }
    }
    
    // Conditional expressions can use:
    // • Any valid C# expression
    // • Variables in scope
    // • Method calls (some limitations)
    // • String comparisons: name == "test"
}
```

### Hit Count Breakpoints

```csharp
public class HitCountBreakpoints
{
    public void Loop()
    {
        for (int i = 0; i < 1000; i++)
        {
            // Right-click breakpoint → Hit Count
            
            // Hit count options:
            // "break always" - every time (default)
            // "break when hit count equals 500" - exactly 500th time
            // "break when hit count is a multiple of 100" - every 100
            // "break when hit count is greater than or equal to 900" - last 100
            
            DoWork(i);
        }
    }
}
```

### Tracepoints (Print to Output)

```csharp
public class Tracepoints
{
    // Tracepoint = breakpoint that prints message without stopping
    
    public void ProcessOrder(Order order)
    {
        // Set breakpoint, right-click → Actions
        // Check "Continue execution"
        // Message: "Processing order {order.Id}, Total: {order.Total}"
        
        // Output window shows:
        // Processing order 123, Total: $99.99
        // Processing order 124, Total: $149.99
        
        // Useful for logging without modifying code
        // Can use: {variableName} for values
        
        // Examples:
        // "i = {i}, result = {result}"
        // "Thread: {System.Threading.Thread.CurrentThread.ManagedThreadId}"
        
        Process(order);
    }
}
```

### Filter Breakpoints

```csharp
public class FilterBreakpoints
{
    // Break only on specific thread, process, or machine
    
    public void MultiThreaded()
    {
        // Right-click breakpoint → Filter
        
        // Filter examples:
        // ThreadName == "WorkerThread"
        // ThreadId == 12345
        // ProcessName == "MyApp.exe"
        
        // Combine with conditions:
        // ThreadId == 12345 && itemCount > 10
        
        // Useful for:
        // • Multi-threaded debugging
        // • Parallel processing issues
        // • Race condition investigation
    }
}
```

### Breakpoint Labels and Groups

```csharp
public class BreakpointLabels
{
    // Organize breakpoints with labels
    
    public void Feature1()
    {
        // Set breakpoint → Right-click → Edit Labels
        // Add label: "Feature1"
        Step1();
        Step2();
    }
    
    public void Feature2()
    {
        // Set breakpoint → Add label: "Feature2"
        ProcessData();
    }
    
    // Breakpoints window:
    // Can filter by label
    // Enable/disable by label
    // Export/import by label
}
```

### Export and Import Breakpoints

```
Breakpoints Window → Toolbar
----------------------------
• Export breakpoints to XML file
• Import breakpoints from file
• Share breakpoints with team
• Version control breakpoint files

Usage:
1. Debug → Windows → Breakpoints (Ctrl + D, B)
2. Click Export button
3. Save .xml file
4. Team member imports file
```

---

## 11. Watch and Immediate Windows

The Watch and Immediate windows are powerful tools for inspecting and manipulating program state during debugging. The Watch window lets you monitor variables and expressions continuously, while the Immediate window allows you to execute code and evaluate expressions on the fly. Together, they provide unparalleled control over debugging sessions.

### Watch Window

```csharp
public class WatchWindow
{
    public void ProcessData(List<int> numbers)
    {
        var filtered = numbers.Where(n => n > 50).ToList();
        var sum = filtered.Sum();
        var average = filtered.Average();
        
        // WATCH WINDOW (Ctrl + D, W or Ctrl + Alt + W, 1)
        // Add expressions to monitor during debugging
        
        // BASIC WATCHES:
        // numbers          - View entire list
        // filtered         - View filtered list
        // sum              - Current value
        // average          - Current value
        
        // COMPLEX EXPRESSIONS:
        // numbers.Count                        - List count
        // filtered.Where(x => x > 80).ToList() - Sub-filter
        // string.Join(", ", filtered)          - Formatted output
        // numbers.Average()                    - Method calls
        
        // OBJECT WATCHES:
        // this              - Current object
        // this._items       - Private field
        // numbers[0]        - Index access
    }
    
    // 4 Watch windows available: Ctrl + Alt + W, 1-4
    // Useful for organizing related expressions
}
```

### Immediate Window

```csharp
public class ImmediateWindow
{
    // IMMEDIATE WINDOW (Ctrl + D, I)
    // Execute code and evaluate expressions during debugging
    
    public void Example()
    {
        string name = "Hello";
        int count = 10;
        
        // Set breakpoint and break here
        
        // EVALUATION:
        // > name
        // "Hello"
        // > count * 2
        // 20
        // > name.ToUpper()
        // "HELLO"
        
        // EXECUTING CODE:
        // > count = 20
        // 20  (variable changed)
        // > name = "World"
        // "World"
        
        // CREATING OBJECTS:
        // > var list = new List<int> { 1, 2, 3 }
        // > list.Sum()
        // 6
        
        // CALLING METHODS:
        // > Console.WriteLine("Test")
        // Test (outputs to console)
        
        // COMMANDS:
        // > ? name          - Evaluate (same as just name)
        // > ?? name         - Evaluate and add to Watch
        // > > cmd           - Execute command (if ambiguous)
        // > cls             - Clear window
    }
}
```

### Make Object ID

```csharp
public class MakeObjectId
{
    public void Example()
    {
        var order1 = new Order { Id = 1 };
        var order2 = order1;
        var order3 = new Order { Id = 1 };
        
        // In Watch or Locals window:
        // Right-click order1 → Make Object ID
        
        // Creates: order1 = $1
        // Now can track this specific instance
        
        // Even when variable goes out of scope,
        // $1 still references the object
        
        // Useful for:
        // • Tracking objects through execution
        // • Verifying reference equality
        // • Following objects in complex scenarios
    }
}
```

### Autos and Locals Windows

```csharp
public class AutosAndLocals
{
    // LOCALS WINDOW (Ctrl + D, L)
    // Shows all local variables in current scope
    
    public void Process(int[] data)
    {
        int sum = 0;           // Visible in Locals
        int count = data.Length; // Visible in Locals
        
        for (int i = 0; i < count; i++) // i visible in Locals
        {
            sum += data[i];
        }
        
        // AUTOS WINDOW (Ctrl + D, A)
        // Shows variables used in current/previous lines
        // Automatically figures out relevant variables
        
        // When stopped on "sum += data[i]":
        // Autos shows: data, i, data[i], sum
    }
}
```

---

## 12. Solution Explorer Tricks

The Solution Explorer is your primary interface for managing projects and files. Beyond basic file navigation, it offers powerful features for searching, filtering, and organizing your codebase. Mastering these tricks helps you work efficiently even with large solutions containing hundreds of projects and thousands of files.

### Essential Solution Explorer Shortcuts

```
Solution Explorer Navigation
----------------------------
Ctrl + Alt + L       = Focus Solution Explorer
Ctrl + ;             = Search in Solution Explorer
Ctrl + [ , S         = Sync with Active Document
Enter                = Open selected file
Right Arrow          = Expand node
Left Arrow           = Collapse node
F2                   = Rename file/folder
Delete               = Delete file/folder
Shift + Delete       = Delete permanently (bypass recycle bin)
```

### Search and Filter

```
Search in Solution Explorer (Ctrl + ;)
--------------------------------------
• Search files, folders, types
• Supports wildcards: *.cs, *Controller*
• Search within files for content

Examples:
• "HomeController" → Find HomeController.cs
• "*.csproj" → Find all project files
• "Service" → Find any file/folder containing "Service"

Filter Solution:
Right-click solution → Filter →
• Show All Files (reveal hidden items)
• Filter by Project Type
• Filter by File Type
```

### Sync with Active Document

```csharp
// Ctrl + [ , S = Sync with Active Document
// Automatically selects current file in Solution Explorer

// Enable auto-sync:
// Tools → Options → Projects and Solutions → General
// ☑ Track Active Item in Solution Explorer

// Now Solution Explorer always highlights current file
// Great for large solutions with deep folder structures
```

### Scope to This

```
Focus on Single Project/Folder
------------------------------
Right-click project → "Scope to This"

Solution Explorer shows only that project
Great for:
• Large solutions
• Focusing on one component
• Reducing visual noise

To exit: Click home icon in Solution Explorer toolbar
```

### Solution Explorer Context Menu Tricks

```
Power User Context Menu Items
-----------------------------
Right-click file:
• Open With... → Choose different editor
• View in Browser (for web files)
• Copy as Path → Full file path to clipboard
• Open Containing Folder → Windows Explorer
• Compare... → Compare with another file (with extension)

Right-click project:
• Add → Existing Item...
• Add → New Folder
• Add Reference...
• Manage NuGet Packages...
• Set as Startup Project

Right-click solution:
• Add → New Project
• Add → Existing Project
• Configure Startup Projects... → Multiple startup
• Project Dependencies... → Build order
```

### Class View Integration

```
Class View (Ctrl + Shift + C)
-----------------------------
Shows classes, interfaces, enums organized by type
Different view than Solution Explorer

Benefits:
• See all types regardless of file
• View inheritance hierarchy
• Quick navigation to members
• See partial classes combined

Sync Class View with Editor:
• Navigate → Sync Class View (in Class View toolbar)
```

---

## 13. Find and Replace Mastery

Visual Studio's Find and Replace features go far beyond simple text search. With regular expressions, file-scoped searches, and replace patterns, you can make complex transformations across your entire codebase. Understanding these capabilities helps you refactor code, fix patterns of errors, and navigate code efficiently.

### Basic Find and Replace

```
Find and Replace Windows
------------------------
Ctrl + F           = Find in current document
Ctrl + H           = Find and Replace in current document
Ctrl + Shift + F   = Find in Files
Ctrl + Shift + H   = Replace in Files

Quick Find Options:
• Match case
• Match whole word
• Use Regular Expressions
• Search up/down
```

### Regular Expression Search

```csharp
// Regex patterns for common searches

// Find all integer variables
// Pattern: int\s+\w+\s*=
int count = 0;
int index = 5;

// Find all string literals
// Pattern: "[^"]*"
string message = "Hello World";

// Find method calls with specific pattern
// Pattern: \w+\([^)]*\)
ProcessData(id);
ValidateInput(name, value);

// Find TODO comments
// Pattern: //\s*TODO.*
// TODO: Implement this
// TODO: Refactor later

// Find properties with specific accessor
// Pattern: public\s+\w+\s+\w+\s*\{\s*get;
public int Id { get; set; }
public string Name { get; set; }

// Find try-catch blocks with empty catch
// Pattern: catch\s*\([^)]+\)\s*\{\s*\}
catch (Exception) { }
```

### Regex Replace Patterns

```csharp
// BEFORE: Convert private fields to use underscore prefix
private int count;
private string name;
private decimal price;

// Find: private\s+(\w+)\s+(\w+);
// Replace: private $1 _$2;

// AFTER:
private int _count;
private string _name;
private decimal _price;

// REGEX REPLACE GROUPS:
// $1, $2, $3... = Captured groups
// ${name} = Named group
// $$ = Literal $

// BEFORE: Convert method calls
GetValue();
GetName();

// Find: Get(\w+)\(\)
// Replace: Get$1() → Fetch$1()

// AFTER:
FetchValue();
FetchName();
```

### Find in Files Options

```
Find in Files (Ctrl + Shift + F)
--------------------------------
Look in:
• Current Document
• Current Project
• Entire Solution
• All Open Documents
• Custom directory set

File Types:
• *.cs           - C# files only
• *.cs,*.xaml    - Multiple types
• !*\bin\*\*     - Exclude bin folders
• *.cs!AssemblyInfo.cs - Exclude specific files

Search Options:
• Keep modified files open
• Display file names only
• Context lines before/after
```

### Find All References

```csharp
// Shift + F12 = Find All References
// Shows every location where symbol is used

public class ReferenceExample
{
    public void Method1()
    {
        ProcessOrder(); // Reference found
    }
    
    public void Method2()
    {
        ProcessOrder(); // Reference found
        ProcessOrder(); // Reference found
    }
    
    private void ProcessOrder()
    {
        // Definition
    }
}

// References window shows:
// • Location (file, line)
// • Context (surrounding code)
// • Project
// • Can group/filter results
```

---

## 14. Bookmarks and Navigation Aids

When working with large codebases, you often need to jump between multiple locations. Bookmarks and other navigation aids help you mark important locations and move between them quickly. These features are especially valuable during debugging sessions or when refactoring code across multiple files.

### Bookmarks

```csharp
// BOOKMARK SHORTCUTS
// Ctrl + K, Ctrl + K = Toggle Bookmark
// Ctrl + K, Ctrl + N = Next Bookmark
// Ctrl + K, Ctrl + P = Previous Bookmark
// Ctrl + K, Ctrl + L = Clear All Bookmarks

public class BookmarkExample
{
    public void Method1()
    {
        // Bookmark here (Ctrl+K, Ctrl+K)
        // Marker appears in margin
    }
    
    public void Method2()
    {
        // Another bookmark
        // Jump between with Ctrl+K, Ctrl+N
    }
    
    public void Method3()
    {
        // Bookmarks persist across sessions
        // View in Bookmarks window (Ctrl+K, Ctrl+W)
    }
}

// BOOKMARK WINDOW (Ctrl + K, Ctrl + W)
// • See all bookmarks
// • Rename bookmarks
// • Create bookmark folders
// • Navigate with double-click
// • Enable/disable bookmarks
```

### Task List Comments

```csharp
// View → Task List (Ctrl + \, T)
// Comments with special tokens appear in Task List

public class TaskListExample
{
    // TODO: Implement error handling
    public void Incomplete()
    {
    }
    
    // HACK: Temporary workaround for bug #123
    public void Workaround()
    {
    }
    
    // NOTE: This method is called from multiple threads
    public void ThreadAware()
    {
    }
    
    // UNDONE: Removed feature, restore later
    public void Removed()
    {
    }
}

// Custom tokens:
// Tools → Options → Environment → Task List
// Add custom tokens: BUGFIX, REVIEW, IMPORTANT
```

### Navigation Bar

```csharp
// NAVIGATION BAR (top of editor window)
// Left dropdown: Types in current file
// Right dropdown: Members of selected type

public class NavigationBarExample
{
    private int _id;
    public int Id => _id;
    
    public void Method1() { }
    public void Method2() { }
    
    // Type "Navigation" in left dropdown to find class
    // Type "Method" in right dropdown to find methods
}

// NAVIGATION BAR SHORTCUTS
// Ctrl + F2 = Focus Navigation Bar
// Tab = Switch between dropdowns
// Enter = Select and go to
// Esc = Return to editor
```

---

## 15. Code Cleanup and Formatting

Clean, consistently formatted code is easier to read, understand, and maintain. Visual Studio provides powerful formatting and cleanup features that can automatically fix style issues, organize usings, and apply team conventions. These tools help you focus on writing code while the editor handles the formatting.

### Format Document

```csharp
// FORMATTING SHORTCUTS
// Ctrl + K, Ctrl + D = Format Document
// Ctrl + K, Ctrl + F = Format Selection

// BEFORE FORMATTING:
public class MessyCode{public void Method(){int x=1;string y="test";
if(x==1){y="changed";}}}

// AFTER Ctrl + K, Ctrl + D:
public class MessyCode
{
    public void Method()
    {
        int x = 1;
        string y = "test";
        if (x == 1) { y = "changed"; }
    }
}
```

### Code Style Configuration

```csharp
// Tools → Options → Text Editor → C# → Code Style

// CONFIGURABLE STYLE RULES:
// • var vs explicit type
// • Predefined type keywords (string vs String)
// • Modifier preferences (readonly, static)
// • Parentheses preferences
// • Expression-level preferences

// Example: Prefer explicit type for non-obvious types
// Code Style: "Prefer explicit type" when "elsewhere"
var text = "hello";        // Style warning if configured
string text = "hello";     // Preferred

// Severity levels:
// • None (silent)
// • Suggestion (gray dots)
// • Warning (green squiggle)
// • Error (red squiggle)
```

### Organize Usings

```csharp
// ORGANIZE USINGS
// Ctrl + R, Ctrl + G = Remove and Sort Usings

using System;
using System.Collections.Generic;  // Unused
using System.Linq;
using System.Threading.Tasks;       // Unused
using Newtonsoft.Json;             // Unused
using System.IO;

public class Example
{
    // Only System and System.Linq actually used
}

// AFTER Ctrl + R, Ctrl + G:
using System;
using System.Linq;

public class Example
{
    // Clean using statements
}

// AUTO-ON-SAVE:
// Tools → Options → Text Editor → C# → Advanced
// ☑ Remove and Sort Usings on Save
```

### EditorConfig for Team Consistency

```ini
# .editorconfig file in project root
# Team-wide formatting settings

# EditorConfig is awesome: https://EditorConfig.org

# top-most EditorConfig file
root = true

# All files
[*]
indent_style = space
indent_size = 4
end_of_line = crlf
charset = utf-8
trim_trailing_whitespace = true
insert_final_newline = true

# C# files
[*.cs]
# New line preferences
csharp_new_line_before_open_brace = all
csharp_new_line_before_else = true
csharp_new_line_before_catch = true
csharp_new_line_before_finally = true

# Indentation preferences
csharp_indent_case_contents = true
csharp_indent_switch_labels = true

# Space preferences
csharp_space_after_cast = false
csharp_space_after_keywords_in_control_flow_statements = true
csharp_space_between_parentheses = false

# Formatting options
csharp_preserve_single_line_statements = false
csharp_preserve_single_line_blocks = true

# Style rules
csharp_prefer_var_over_explicit_type = true:suggestion
dotnet_style_predefined_type_for_locals_parameters_members = true:suggestion
dotnet_style_predefined_type_for_member_access = true:suggestion
```

### Code Cleanup Profile

```
Code Cleanup (Ctrl + K, Ctrl + E)
---------------------------------
Run multiple fixes at once

Default profile includes:
• Fix code style
• Sort usings
• Remove unnecessary usings
• Apply implicit/explicit type preferences
• Add accessibility modifiers

Create custom profiles:
1. Tools → Options → Text Editor → C# → Code Cleanup
2. Create new profile
3. Select which fixes to apply
4. Run with Ctrl + K, Ctrl + E

Can run on:
• Current document
• Selection
• Entire project
• Entire solution
```

---

## 16. Live Templates and Code Generation

Visual Studio can generate code for you, from simple property declarations to entire class implementations. Understanding these code generation features helps you write code faster and ensures consistency. From generating constructors to implementing interfaces, these features eliminate boilerplate coding.

### Generate Constructor

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    public decimal Price { get; set; }
    
    // QUICK ACTION: Generate Constructor
    // Ctrl + . → "Generate constructor"
    
    // Option 1: Generate with no parameters
    public Product() { }
    
    // Option 2: Generate with properties
    public Product(int id, string name, decimal price)
    {
        Id = id;
        Name = name;
        Price = price;
    }
    
    // Option 3: Generate from base class
}
```

### Generate Equals and GetHashCode

```csharp
public class Product
{
    public int Id { get; set; }
    public string Name { get; set; }
    
    // Ctrl + . → "Generate Equals and GetHashCode"
    
    public override bool Equals(object obj)
    {
        return obj is Product product &&
               Id == product.Id &&
               Name == product.Name;
    }
    
    public override int GetHashCode()
    {
        return HashCode.Combine(Id, Name);
    }
}
```

### Generate Overrides

```csharp
public class CustomException : Exception
{
    // Type "override" and IntelliSense shows overridable members
    // Or Ctrl + . → "Generate overrides"
    
    public override string Message => "Custom message";
    
    public override string ToString()
    {
        return $"CustomException: {Message}";
    }
}
```

### Implement Interface

```csharp
public class OrderRepository : IRepository<Order>
{
    // Ctrl + . → "Implement interface"
    // or "Implement interface explicitly"
    
    public Order GetById(int id)
    {
        throw new NotImplementedException();
    }
    
    public List<Order> GetAll()
    {
        throw new NotImplementedException();
    }
    
    public void Add(Order entity)
    {
        throw new NotImplementedException();
    }
    
    // Implement explicitly:
    // IRepository<Order>.GetById(int id)
}
```

### Generate Method from Usage

```csharp
public class GenerateFromUsage
{
    public void Example()
    {
        // Type method that doesn't exist:
        var result = CalculateTotal(100, 0.08m);
        
        // Ctrl + . → "Generate method"
        // Generated:
    }
    
    private decimal CalculateTotal(decimal v1, decimal v2)
    {
        throw new NotImplementedException();
    }
}

// Can also generate:
// • Classes
// • Properties
// • Fields
// • Parameters
```

---

## 17. File and Window Management

Visual Studio provides extensive window management capabilities for customizing your development environment. Learning to manage windows efficiently helps you maximize screen real estate and maintain focus on relevant code. From tabbed documents to floating windows, these features let you create your ideal workspace.

### Tab Management

```
TAB SHORTCUTS
-------------
Ctrl + Tab              = Switch between open files
Ctrl + Shift + Tab      = Switch backwards
Ctrl + F4               = Close current tab
Ctrl + Shift + F4       = Close current tab (alternative)

Ctrl + Click tab        = Open in new group
Right-click tab → Float = Make window floating
Right-click tab → Dock  = Dock to main area

PIN TABS
--------
Pin important tabs to keep them open
Pinned tabs appear on left side
Click pin icon or right-click → Pin Tab

TAB LAYOUT OPTIONS
------------------
Tools → Options → Environment → Tabs and Windows
• Show pin tabs in separate row
• Insert new tabs to the right
• Preview tab behavior
```

### Window Layout

```
WINDOW SHORTCUTS
----------------
Ctrl + #, #            = Focus specific window
                       (# = digit on numpad or row)

Ctrl + `               = Toggle command window
Ctrl + Alt + L         = Solution Explorer
Ctrl + \, E            = Error List
Ctrl + \, T            = Task List
Ctrl + Alt + O         = Output Window

AUTO HIDE
---------
Auto-hide button on window title bar
Window slides to edge when not focused
Hover to show, click elsewhere to hide

FLOATING WINDOWS
----------------
Drag window outside main area
Great for:
• Multiple monitors
• Reference material
• Debugging windows
```

### Split View

```csharp
// SPLIT EDITOR VERTICALLY
// Window → New Window (creates second view)
// Or drag tab to right side

// SPLIT EDITOR HORIZONTALLY
// Grab split bar at top of scroll bar
// Drag down to split

public class SplitViewExample
{
    // View top of file in one split
    public void TopMethod()
    {
    }
    
    // Large code section...
    // ...
    // ...
    
    // View bottom of file in other split
    public void BottomMethod()
    {
        // Can see top and bottom simultaneously
        // Edit in either view
    }
}
```

### Full Screen Mode

```
FULL SCREEN
-----------
Shift + Alt + Enter = Toggle Full Screen Mode

Hides:
• Menu bar
• Tool windows
• Tabs (optional)
• Status bar

Great for:
• Presentations
• Focused coding
• Small screens

ESC = Exit full screen
```

### Save and Load Window Layouts

```
WINDOW LAYOUTS
--------------
Window → Save Window Layout
Window → Apply Window Layout
Window → Manage Window Layouts

Save different layouts for:
• Coding
• Debugging
• Design work
• Presentations

Layouts persist:
• Tool window positions
• Docked/floating state
• Auto-hide settings
```

---

## 18. Git and Source Control Shortcuts

Visual Studio has excellent Git integration built directly into the IDE. Understanding Git shortcuts and features helps you manage source control efficiently without leaving the editor. From committing changes to resolving merge conflicts, these features streamline your workflow.

### Git Shortcuts

```
GIT SHORTCUTS
-------------
Ctrl + M, G           = Go to Git Changes
Ctrl + 0, G           = View Git Changes window
Ctrl + 0, C           = Commit changes

COMMON GIT TASKS
----------------
Git → Changes              = View pending changes
Git → Branches             = Manage branches
Git → Sync                 = Fetch/Pull/Push
Git → Manage Remotes       = Configure remotes

INLINE GIT BLAME
----------------
Hover over code line → See author and commit
Click → View full commit details

TOOLS → OPTIONS → SOURCE CONTROL
--------------------------------
• Enable inline blame
• Configure diff tools
• Set up external merge tool
```

### Git Changes Window

```
GIT CHANGES WINDOW
------------------
Shows:
• Modified files
• New files
• Deleted files
• Untracked files

Actions:
• Stage individual changes
• Stage all
• Commit
• Commit and Push
• Commit and Sync

Double-click file = View diff
Right-click = View history, blame, etc.
```

### Merge Conflicts

```csharp
// When merge conflict occurs:

// <<<<<<< HEAD
// var result = CalculateTotal(items);
// =======
// var result = ComputeTotal(items);
// >>>>>>>>>> feature-branch

// Visual Studio shows conflict markers
// Click to accept:
// • Accept Current (HEAD)
// • Accept Incoming (feature-branch)
// • Accept Both
// • Compare changes

// Resolve manually in merge editor
// Shows side-by-side comparison
```

### Git History

```
VIEW FILE HISTORY
-----------------
Right-click file → Git → View History

Shows:
• All commits affecting file
• Authors
• Dates
• Commit messages
• Lines changed

Click commit = View changes at that point
Double-click = View file at that commit
```

---

## 19. Testing Shortcuts and Tricks

Visual Studio provides comprehensive testing tools for unit tests, integration tests, and more. Understanding testing shortcuts helps you run and debug tests efficiently, making TDD and test maintenance much easier.

### Test Explorer

```
TEST EXPLORER SHORTCUTS
-----------------------
Ctrl + E, T           = Run all tests
Ctrl + E, S           = Run selected test
Ctrl + E, D           = Debug selected test
Ctrl + E, L           = Open Test Explorer

TEST EXPLORER WINDOW
--------------------
Test → Test Explorer

Features:
• Group by project/class
• Search and filter tests
• Run/Debug individual tests
• View test results
• Code coverage (Enterprise)
```

### Running Tests

```csharp
using Microsoft.VisualStudio.TestTools.UnitTesting;

[TestClass]
public class CalculatorTests
{
    [TestMethod]
    public void Add_TwoNumbers_ReturnsSum()
    {
        // Arrange
        var calc = new Calculator();
        
        // Act
        var result = calc.Add(2, 3);
        
        // Assert
        Assert.AreEqual(5, result);
    }
    
    // RUNNING TESTS:
    // Click test icon in margin → Run/Debug
    // Right-click test method → Run Tests
    // Right-click test class → Run All Tests in Class
    // Ctrl + R, T = Run tests in current context
    // Ctrl + R, Ctrl + T = Debug tests in current context
    
    [TestMethod]
    [DataRow(1, 2, 3)]
    [DataRow(5, 5, 10)]
    [DataRow(-1, 1, 0)]
    public void Add_VariousInputs_ReturnsSum(int a, int b, int expected)
    {
        var calc = new Calculator();
        Assert.AreEqual(expected, calc.Add(a, b));
    }
}
```

### Live Unit Testing (Enterprise)

```
LIVE UNIT TESTING
-----------------
Test → Live Unit Testing → Start

Shows test results inline:
• Green checkmark = Passing
• Red X = Failing
• Blue line = Covered by test

Benefits:
• Instant feedback
• See which tests cover your code
• Identify untested code paths

Configure:
Test → Live Unit Testing → Options
```

---

## 20. Performance Profiler Tips

Visual Studio includes powerful profiling tools that help you identify performance bottlenecks in your applications. Understanding these tools helps you optimize code and deliver faster applications.

### Profiling Tools

```
START PROFILING
---------------
Debug → Performance Profiler
Alt + F2

AVAILABLE PROFILERS:
• CPU Usage
• Memory Usage
• .NET Object Allocation
• GPU Usage
• Database (for EF)
• Instrumentation

QUICK PROFILING:
Right-click project → Profile
```

### CPU Profiling

```
CPU USAGE PROFILER
------------------
1. Start profiling session
2. Exercise your code
3. Stop and analyze

Shows:
• Hot paths
• Time in each function
• Call trees
• Flame graphs

Tips:
• Focus on hot paths
• Look for unnecessary calls
• Check for repeated operations
```

### Memory Profiling

```
MEMORY USAGE PROFILER
---------------------
Shows:
• Object counts
• Memory allocations
• Gen 0/1/2 collections
• Large object heap

Tips:
• Look for memory leaks
• Check object lifetimes
• Watch for excessive allocations

SNAPSHOT COMPARISON:
Take snapshots at different times
Compare to find leaks
```

---

## 21. Extension Recommendations

Extensions enhance Visual Studio with additional features and capabilities. Here are the most valuable extensions for productivity.

### Essential Extensions

```
PRODUCTIVITY
------------
• Productivity Power Tools - Microsoft's productivity boost
• ReSharper - Ultimate productivity suite (paid)
• CodeMaid - Code cleanup and organization
• Visual Commander - Command automation

THEMES AND APPEARANCE
---------------------
• Color Themes for Visual Studio
• JetBrains Darcula Theme
• Solarized Theme

CODE ANALYSIS
-------------
• SonarLint - Real-time code analysis
• Roslynator - Code refactorings
• Error Shutup - Suppress specific warnings

GIT AND SOURCE CONTROL
----------------------
• GitFlow Extension - GitFlow workflow
• GitHub Extension for Visual Studio

TESTING
-------
• NCrunch - Continuous testing (paid)
• Xunit.Guard - Test generation

OTHER
-----
• OzCode - Enhanced debugging (paid)
• Output Enhancer - Color-coded output
• File Differ - File comparison
```

### Extension Manager

```
MANAGE EXTENSIONS
-----------------
Extensions → Manage Extensions

Categories:
• Installed
• Online (browse new)
• Updates

Tips:
• Check for updates regularly
• Disable unused extensions
• Remove conflicting extensions
• Some extensions require restart
```

---

## 22. C# Language Tricks

Beyond Visual Studio features, C# itself offers many language features and tricks that improve productivity.

### Null Checking

```csharp
// NULL-COALESCING OPERATOR
string name = input ?? "default";

// NULL-COALESCING ASSIGNMENT
name ??= "default";  // Assigns if null

// NULL-CONDITIONAL OPERATOR
int? length = customer?.Address?.Length;

// NULL-CONDITIONAL WITH INDEXER
char? firstChar = name?[0];

// COMBINED
string result = customer?.Name ?? "Unknown";
```

### Pattern Matching

```csharp
// TYPE PATTERNS
if (obj is string s)
{
    Console.WriteLine(s.Length);
}

// PROPERTY PATTERNS
if (order is { Status: OrderStatus.Completed, Total: > 100 })
{
    // Order is completed with total > 100
}

// SWITCH EXPRESSIONS
string GetDescription(int value) => value switch
{
    0 => "Zero",
    < 10 => "Single digit",
    < 100 => "Double digit",
    _ => "Large"
};

// TUPLE PATTERNS
string GetDirection(int x, int y) => (x, y) switch
{
    (0, 0) => "Center",
    (0, _) => "Vertical",
    (_, 0) => "Horizontal",
    _ => "Other"
};
```

### Record Types

```csharp
// CONCISE RECORD DEFINITION
public record Person(string Name, int Age);

// WITH EXPRESSION FOR IMMUTABLE UPDATES
var person = new Person("John", 30);
var olderPerson = person with { Age = 31 };

// RECORD STRUCT
public record struct Point(int X, int Y);

// POSITIONAL PARAMETERS
var p = new Point(10, 20);
var (x, y) = p;  // Deconstruction
```

### Collection Expressions

```csharp
// C# 12 COLLECTION EXPRESSIONS
List<int> list = [1, 2, 3, 4, 5];
int[] array = [1, 2, 3];
HashSet<int> set = [1, 2, 3];

// SPREAD OPERATOR
int[] more = [..list, 6, 7, 8];
// [1, 2, 3, 4, 5, 6, 7, 8]

// EMPTY COLLECTIONS
List<int> empty = [];
```

### Primary Constructors

```csharp
// C# 12 PRIMARY CONSTRUCTORS
public class ProductService(ILogger logger, IProductRepository repository)
{
    public Product GetProduct(int id)
    {
        logger.LogInformation("Getting product {Id}", id);
        return repository.GetById(id);
    }
    
    // Parameters available throughout class
}

// WITH INHERITANCE
public class DiscountedProductService(
    ILogger logger,
    IProductRepository repository,
    decimal discountRate
) : ProductService(logger, repository)
{
}
```

---

## 23. C# Modern Features Shortcuts

### Required Properties

```csharp
public class Product
{
    public required int Id { get; init; }
    public required string Name { get; init; }
    public decimal Price { get; set; }
}

// Compiler requires:
var product = new Product { Id = 1, Name = "Test" };
```

### File-Scoped Namespaces

```csharp
// TRADITIONAL
namespace MyApp.Services
{
    public class Service
    {
    }
}

// FILE-SCOPED (C# 10+)
namespace MyApp.Services;

public class Service
{
}
```

### Global Usings

```csharp
// GlobalUsings.cs
global using System;
global using System.Collections.Generic;
global using System.Linq;
global using System.Threading.Tasks;
global using Microsoft.EntityFrameworkCore;

// Available in all files in project
// Implicit usings can be enabled in project file:
// <ImplicitUsings>enable</ImplicitUsings>
```

### Target-Typed New

```csharp
// BEFORE
List<string> list = new List<string>();
Dictionary<string, int> dict = new Dictionary<string, int>();

// AFTER (target-typed new)
List<string> list = new();
Dictionary<string, int> dict = new();

// Works with method calls
ProcessOrder(new() { Id = 1, Name = "Test" });
```

---

## 24. LINQ and Collection Tricks

### LINQ Shortcuts

```csharp
// METHOD SYNTAX vs QUERY SYNTAX
var result1 = items.Where(x => x > 10).Select(x => x * 2);
var result2 = from x in items where x > 10 select x * 2;

// CHAINED OPERATIONS
var result = orders
    .Where(o => o.Status == OrderStatus.Completed)
    .GroupBy(o => o.CustomerId)
    .Select(g => new { CustomerId = g.Key, Total = g.Sum(o => o.Total) })
    .OrderByDescending(x => x.Total)
    .Take(10);

// DICTIONARY FROM COLLECTION
var dict = items.ToDictionary(x => x.Id, x => x.Name);

// LOOKUP (MULTIPLE VALUES PER KEY)
var lookup = orders.ToLookup(o => o.CustomerId);

// DISTINCT BY (C# 10+ via LINQ)
var unique = items.DistinctBy(x => x.CategoryId);
```

### Collection Initialization

```csharp
// COLLECTION EXPRESSIONS (C# 12)
List<int> numbers = [1, 2, 3, 4, 5];
Dictionary<string, int> dict = new()
{
    ["one"] = 1,
    ["two"] = 2
};

// IMMUTABLE COLLECTIONS
var immutableList = ImmutableList.Create(1, 2, 3);
var builder = ImmutableList.CreateBuilder<int>();
builder.Add(1);
var list = builder.ToImmutable();
```

---

## 25. Async/Await Debugging Tricks

### Debugging Async Code

```csharp
// PARALLEL STACKS WINDOW (Ctrl + D, S)
// Shows all async tasks and their call stacks

// THREADS WINDOW (Ctrl + D, T)
// Shows all threads, including async state

// TASKS WINDOW (Ctrl + D, K)
// Shows all active tasks
// View status, start time, duration

public class AsyncDebugging
{
    public async Task ProcessAsync()
    {
        // Set breakpoint on async method
        // Step through awaits
        // F11 steps into awaited method
        
        await Task.Delay(1000);  // Step over (F10) doesn't wait
        await ProcessDataAsync();
    }
    
    // VIEW AWAITER STATE
    // In Watch window: task.Status, task.IsCompleted
}
```

### ConfigureAwait

```csharp
public class ConfigureAwaitExample
{
    // Library code: Always use ConfigureAwait(false)
    public async Task<string> GetDataAsync()
    {
        using var client = new HttpClient();
        return await client.GetStringAsync("https://api.example.com")
            .ConfigureAwait(false);
    }
    
    // UI code: Don't use ConfigureAwait (need UI context)
    public async void Button_Click(object sender, EventArgs e)
    {
        var data = await GetDataAsync();  // Captures UI context
        textBox.Text = data;  // Safe to update UI
    }
}
```

---

## 26. Error List and Output Window

### Error List

```
ERROR LIST WINDOW
-----------------
Ctrl + \, E  or  Ctrl + W, E

Shows:
• Errors
• Warnings
• Messages

Filter by:
• Project
• Document
• Severity

Double-click = Go to error
Right-click = Copy, suppress, etc.

SHORTCUTS
---------
F8 = Next error
Shift + F8 = Previous error
```

### Output Window

```
OUTPUT WINDOW
-------------
Ctrl + Alt + O

Shows output from:
• Build
• Debug
• Source Control
• Tests
• Custom tools

Filter by dropdown at top
Right-click = Clear, Copy
```

---

## 27. Customization and Options

### Essential Settings

```
TOOLS → OPTIONS (Ctrl + Q, type "options")
------------------------------------------

TEXT EDITOR → C#
• General: Line numbers, word wrap
• Tabs: Insert spaces, tab size 4
• Code Style: Configure preferences
• Advanced: Enable/disabled features

ENVIRONMENT
• General: Window menu items, status bar
• Fonts and Colors: Editor theme
• Keyboard: Customize shortcuts
• Startup: What opens on launch

DEBUGGING
• General: Step over properties, etc.
• Symbols: Symbol server settings
• Edit and Continue: Enable/disable

PROJECTS AND SOLUTIONS
• General: Track active item
• Build and Run: What happens on run
```

### Custom Keyboard Shortcuts

```
CREATE CUSTOM SHORTCUT
----------------------
Tools → Options → Environment → Keyboard

1. Find command in list
2. Press shortcut keys
3. Click Assign

Popular customizations:
• Build.RebuildSolution: Ctrl+Shift+B
• Debug.StartWithoutDebugging: Ctrl+F5
• Edit.FormatDocument: Ctrl+K, D

IMPORT/EXPORT SETTINGS
----------------------
Tools → Import and Export Settings
• Export current settings
• Import saved settings
• Reset to defaults
```

---

## 28. Productivity Power Tools

### Must-Have Features

```
PRODUCTIVITY POWER TOOLS (Extension)
------------------------------------
Install from: Extensions → Manage Extensions

FEATURES:
• Fix Mixed Tabs - Auto-fix tab/space issues
• Middle Click Close - Close tabs with middle-click
• Copy/Cut Current Line - Without selection
• Quick Launch - Enhanced search
• Peek Definition - Preview without navigation
• Structure Visualizer - Code structure lines
• Match Margin - Highlight matching braces
• Scroll Bar Marks - See errors in scroll bar
```

---

## 29. Cross-Platform Development Tips

### .NET MAUI / Xamarin

```
XAML PREVIEWER
--------------
View → Other Windows → XAML Previewer

Shows live preview of XAML UI
Hot Reload enabled by default

ANDROID EMULATOR
----------------
Tools → Android → Android Device Manager

Create and manage virtual devices
```

### Docker

```
DOCKER SUPPORT
--------------
Right-click project → Add → Docker Support

CONTAINER TOOLS
---------------
View → Other Windows → Containers

Shows:
• Running containers
• Images
• Volumes
• Logs
```

---

## 30. Expert-Level Shortcuts

### The Ultimate Shortcut List

```
┌─────────────────────────────────────────────────────────────┐
│                   EXPERT SHORTCUTS                           │
├─────────────────────────────────────────────────────────────┤
│ NAVIGATION                                                   │
│ Ctrl + ,         Navigate To (everything search)            │
│ Ctrl + T         Go To File                                 │
│ Ctrl + 1, T      Go To Type                                 │
│ Ctrl + 1, M      Go To Member                               │
│ Ctrl + G         Go To Line                                 │
│ F12              Go To Definition                           │
│ Ctrl + F12       Go To Declaration                          │
│ Shift + F12      Find All References                        │
│ Alt + F12        Peek Definition                            │
│ Ctrl + -         Navigate Backward                          │
│ Ctrl + Shift + - Navigate Forward                           │
├─────────────────────────────────────────────────────────────┤
│ EDITING                                                      │
│ Ctrl + K, C      Comment Selection                          │
│ Ctrl + K, U      Uncomment Selection                        │
│ Ctrl + K, D      Format Document                            │
│ Ctrl + K, F      Format Selection                           │
│ Ctrl + M, M      Toggle Outlining                           │
│ Ctrl + M, O      Collapse to Definitions                    │
│ Ctrl + K, S      Surround With                              │
│ Ctrl + K, X      Insert Snippet                             │
│ Ctrl + K, K      Toggle Bookmark                            │
├─────────────────────────────────────────────────────────────┤
│ REFACTORING                                                  │
│ Ctrl + .         Quick Actions                              │
│ F2               Rename                                     │
│ Ctrl + R, R      Rename                                     │
│ Ctrl + R, M      Extract Method                             │
│ Ctrl + R, I      Extract Interface                          │
│ Ctrl + R, E      Encapsulate Field                          │
├─────────────────────────────────────────────────────────────┤
│ DEBUGGING                                                    │
│ F5               Start Debugging                            │
│ Ctrl + F5        Start Without Debugging                    │
│ F9               Toggle Breakpoint                          │
│ F10              Step Over                                  │
│ F11              Step Into                                  │
│ Shift + F11      Step Out                                   │
│ Ctrl + F10       Run to Cursor                              │
│ Ctrl + D, I      Immediate Window                           │
│ Ctrl + D, W      Watch Window                               │
├─────────────────────────────────────────────────────────────┤
│ WINDOW MANAGEMENT                                            │
│ Ctrl + Tab        Switch Documents                          │
│ Ctrl + F4         Close Document                            │
│ Ctrl + Alt + L    Solution Explorer                         │
│ Ctrl + \, E       Error List                                │
│ Shift + Alt + Enter Full Screen                            │
│ Ctrl + Q          Quick Launch                              │
└─────────────────────────────────────────────────────────────┘
```

### Speed Techniques

```
MASTER THESE TECHNIQUES
-----------------------

1. QUICK LAUNCH (Ctrl + Q)
   Type anything to find commands, options, files

2. NAVIGATE TO (Ctrl + ,)
   Find anything in solution by name

3. PEEK DEFINITION (Alt + F12)
   View code without losing context

4. QUICK ACTIONS (Ctrl + .)
   Context-aware fixes and refactorings

5. SNIPPETS (Tab + Tab)
   Insert code templates instantly

6. MULTI-CARET (Ctrl + Alt + Click)
   Edit multiple locations simultaneously

7. CLIPBOARD RING (Ctrl + Shift + V)
   Access clipboard history

8. TASK LIST (Ctrl + \, T)
   Track TODOs and FIXMEs

9. CODE CLEANUP (Ctrl + K, E)
   Fix style issues in bulk

10. WINDOW LAYOUTS
    Save and restore custom layouts
```

---

## Summary

Mastering Visual Studio and C# shortcuts is a journey, not a destination. Start with the essentials—navigation, editing, and debugging shortcuts—and gradually incorporate more advanced techniques into your workflow. The key is consistency: focus on learning one or two new shortcuts each day until they become muscle memory.

The productivity gains from these techniques compound over time. A developer who efficiently navigates code, refactors with confidence, and debugs effectively will consistently outperform one who struggles with their tools. More importantly, these skills reduce cognitive load, allowing you to focus on what matters most: solving problems and building great software.

Remember that the best shortcut is the one you actually use. Don't try to memorize everything at once—bookmark this guide, refer to it when you encounter repetitive tasks, and gradually build your repertoire of productivity techniques. Your future self will thank you for the investment.
