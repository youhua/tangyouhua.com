---
title: "Best Practices for Enhancing Collaboration Between Designers and Developers"
datePublished: Tue Jun 10 2025 10:02:14 GMT+0000 (Coordinated Universal Time)
cuid: cmbqcqn81000c02l7fd612a3d
slug: best-practices-for-enhancing-collaboration-between-designers-and-developers
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/YRUj8BENrVQ/upload/90737e4f973035164b87979354a971ac.jpeg
tags: web-design, web-development, figma, figma-to-code

---

## **First, let's align with the fundamental principles of design thinking**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749440552998/c9fc9e03-061e-4648-8629-6180b86b55bc.png align="center")

As we know, product design involves iterative cycles of understanding, exploring, and materializing.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749441124323/a203482d-e3c1-47ce-867c-21b815a60018.png align="center")

In this process, the further we progress, the more costly it becomes to implement changes. Therefore, I recommend maximizing iterations through rapid prototyping and user testing during the design phase.

## Do your best with prototyping

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749452203193/dfe474de-0def-409f-aea7-6bc83fe84ec5.jpeg align="center")

In traditional engineering, skipping prototyping is unimaginable. You can't wait for a rocket to launch and explode before redesigning and refining its structure. However, in web design, we often overlook or even skip prototyping.

Generally, there are two types of prototypes: wireframe and high fidelity. Each has its appropriate use, and I think we should not skip any stage lightly.

### Wireframes

For wireframes, the focus is on information architecture, user flow, layout, and user interaction. Other visual elements, such as color, background, animation, and shadows, are usually deliberately ignored at this stage.

%[https://youtu.be/iyrEStiTZh0?si=paRC4a1jN0bHFnC_] 

You should repeatedly confirm these questions during the wireframe prototyping and user testing processes:

1. Where should users start?
    
2. What steps must they take to achieve their goals?
    
3. Are there any technical means to simplify these steps?
    
4. What are the most important elements that appear on the screen at each step, and what are their priorities?
    
5. How should the elements be arranged for easier reading and interaction by users on the screens of common devices?
    

**During this process, we can also gain clearer user flows with the help of FigJam:**

![](https://cdn.sanity.io/images/599r6htc/regionalized/66e808bb9e6f0719f68c04385a080c9db39a781d-2330x1651.png?q=75&fit=max&auto=format&dpr=2 align="left")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749457815640/e04f6640-4f2f-44a7-bc52-40d396c7f33d.png align="center")

The more time we spend on this step, the more comprehensive our understanding and consideration of requirements will be, enabling us to avoid unnecessary revisions later on and helping us launch new features sooner.

### **High-fidelity prototypes**

High-fidelity prototypes are detailed UX simulations or fully coded products used for user testing or developer handoff. Ideally, they should look exactly like the final version you will see when it's published. This may seem challenging, but luckily, our existing design library can make this process easier.

%[https://youtu.be/eKVPXk2BnB8] 

### Challenge: Users are not interested in our prototype demonstration!

There are two key steps that could help address this issue:

1. Complete the main [prototype flows](https://help.figma.com/hc/en-us/articles/360039823894-Create-and-manage-prototype-flows) and demonstrate it in [presentation view](https://help.figma.com/hc/en-us/articles/360040318013-Play-your-prototypes#Present_your_prototype) rather than the default edit mode view.
    
    ![A connection is created from one frame to another. A flow starting point is added to the first frame.](https://help.figma.com/hc/article_attachments/31779384389911 align="left")
    
2. ![Prototype Preview.png](https://help.figma.com/hc/article_attachments/31622164892567 align="left")
    
    Change the avatar, name, images, text, and other content as much as possible to make them familiar to your target customers. This helps users feel a sense of connection.
    

Of course, this approach takes a bit more time, but it's still much quicker and more convenient than waiting for the engineering team to write code, set up a database, and deploy it to the preview environment.

## Thinking about the big picture

Many times, we spend weeks or even months hurrying to release a new feature, only to find that nobody is interested. Hardly any users click on those buttons, no matter how appealing we make them, or most users leave before completing the first three steps. Some other times, we change a navigation bar globally for new features, but after release, we encounter unexpected problems with the basic usability of other modules.

### Focus on tracking metrics and user flows from the beginning

It's recommended to clearly define how to measure the feature's success before beginning any future design. This will help us focus on designing events and creating more effective user flows for better conversion.

### Design the different states, such as loading, error, empty status, and other edge cases

Technically, we use the Form component from Ant Design, which includes various interaction and validation states. We should ensure these states match our brand's visual system consistently. This way, the different interaction states of our form components will meet expectations by default, without needing any overrides.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749546880448/dbb4ce43-e8ce-4895-a317-9fe408d2dd1d.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749547186635/a6ae211d-2cd2-4e60-b7d9-4add5ea9e596.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749547113401/66a82166-3c9c-4400-9a4c-8b1559ceea12.png align="center")

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749547017215/dd3717e4-3a72-4b6d-9720-4168e50f8055.png align="center")

The same principle applies to global loading, skeleton, empty states, etc.

### Consider potential conflicts with existing functions or flows as early as possible

A recent example is that we completely restructured the global menu on the left side of the home page, making it look much simpler, but we did not consider how the menu would be displayed under other pages.

As a result, the engineering team first developed a custom solution for the home page, then implemented a global rollout at the request of the product designer. However, after the new static design went live, it became apparent that it was incompatible with many of the old pages, forcing the engineering team to modify the global menu again within a single day. Similar issues continued to arise, posing significant challenges to the stability and user experience of our platform.

How can we address these issues? Before starting any new design, consider these questions:

1. Will these changes affect other pages or modules?
    
2. How will the new design work on mobile devices?
    
3. Should there be variations for different user types (such as different levels of paid subscriptions)?
    
4. Do these variations conflict with existing logic?
    

Listing all the logic branches using a table or mind map can greatly help prevent similar issues. This logic is a crucial part of the product requirements document (PRD) that product designers need to consider carefully. They should think it through thoroughly before handing off the design. This input is essential for the engineering team. Skipping essential design thinking and expecting to constantly ask questions or make patches during development and testing, or frequently applying hot-fixes with each release, does not result in a satisfactory product. Instead, it creates chaos and often frustrates users.

## Always start with a frame that has a predefined size

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749468014834/94f713b6-a385-4710-8ced-694af3f5d4b5.png align="center")

Compared to sections, frames have predefined sizes for the most popular devices. This helps you set the correct scale from the start and consider how your design will look on common devices. Also, frames have the concept of [Constraints](https://help.figma.com/hc/en-us/articles/360039957734-Apply-constraints-to-define-how-layers-resize) and can easily apply layout guide styles from our design system, whereas sections cannot.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749471372206/b8ea33fa-eb35-4673-bc79-bc046769d69d.png align="center")

learn more about the difference between Figma Frames and Sections if you are interested：

%[https://youtu.be/pOJGMjl6X2A?si=knnRIngdEkHt3f9h] 

You don't need to be a Figma expert. Just replace sections with frames and avoid randomly scaling top-level frames can greatly improve basic layout issues.

## Always use the predefined variables

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749472979013/40011e7b-7462-4fd4-9c3b-2fdbe3cea279.png align="center")

## Avoid scale text and layout layers

%[https://youtu.be/nvzvoAvlckU?si=TkGb8ajAj7J3TMDu] 

Please use the move tool and auto layout to resizing with constraints most of the time. This ensures that all border widths, border radius, and font sizes remain unchanged while resizing. The only exception is when you want to resize an object and also adjust its stroke, font size, or other attributes proportionally!

> The scale tool can be handy for situations where you want to resize a group of elements at once. This makes sure all elements, including text, are scaled consistently. It also allows you to ignore other settings, like constraints.
> 
> This can lead to fractional font sizes or layers with subpixel positions and dimensions. Aside from annoying pixel perfectionists, it can also lead to unwanted export artifacts and dimensions.
> 
> If you just want to change the size of a text layer in relation to other elements in a design, we recommend adjusting the [**Font size**](https://help.figma.com/hc/en-us/articles/360039956634-Explore-text-properties#basic) in the **Typography** settings instead. This makes sure your font size is a whole number.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">We currently use the scale tool extensively, but essentially misuse it. The scale tool inevitably results in dimensions that are challenging for developers, such as border widths of 1.785px, font sizes of 13.925px, and border radius of 38.759px.</div>
</div>

## Create and maintain an effective design system

![A library of icons, colors, typeface styles, and spacers](https://cdn.sanity.io/images/599r6htc/regionalized/3f1bfae9ff0fba1b956c69af93cb1b4f33b6381a-1080x864.png?w=780&h=624&q=75&fit=max&auto=format align="left")

A design system is a collection of reusable components, guidelines, and assets that help maintain consistency and efficiency in the design process. It serves as a single source of truth for designers, developers, and stakeholders. Here’s a great [introduction to design systems](https://www.youtube.com/watch?v=YLo6g58vUm0).

Creating a design system involves defining typography styles, color palettes, grid systems, iconography, and other visual elements that align with the brand's identity.

A design system that aligns both design and code can streamlining the product development process:

**Product designers don't need to be Figma experts.** They can **simply select predefined variables, styles, and components.**

All the **font sizes, gaps, padding, spacing, and colors** will be **automatically generated by the design system.** **Developers can simply copy and paste from Figma** without having to think about it. When everything goes well, we no longer need to repeatedly deal with layout and font size issues during testing.

We have had a [design system](https://www.figma.com/design/ogjn6pRFttytQXQNP4g5Qb/%F0%9F%92%8E-Pietra-Design-System?node-id=1539-11377&m=dev) in place for years. However, due to staff changes, there are now a few minor issues. We just need to make some refinements to keep using it smoothly:

1. **Version Control:** We currently have two design systems: [💎 Pietra Design System](https://www.figma.com/design/ogjn6pRFttytQXQNP4g5Qb/%F0%9F%92%8E-Pietra-Design-System?node-id=1539-11377&t=Cw6iPrUr8u8RBM87-0), which was originally created by Kapil and is somewhat outdated, and [🖌️ Design System V2 - WIP](https://www.figma.com/design/aMut15iUN03jwyEIjTJQqk/%F0%9F%96%8C%EF%B8%8F-Design-system-V2---WIP?m=auto&t=aRRlVaQELwkVxmZP-6), which was recently created by Pareshi and currently has only a few variables ready for development. For a code repository with more than five years of history, it is acceptable to have two versions of the design system coexisting. This ensures that our large amount of legacy code remains functional while allowing us to gradually migrate to the new version. I have exported all variables from both design systems into the code. Since they have different naming conventions, we can use them together.
    
2. **Naming conventions:** Custom property names are case-sensitive—`--my-color` is considered a different custom property from `--My-color` in CSS. Therefore, we have a `stylelint` rule to ensure that variable names follow **kebab-case** (keep all letters lowercase and connect words with a hyphen) to avoid potential confusion. As a result, variable names like `XL` and `XXL` in Figma are not valid for code. We need to ensure all variable names are always in lowercase.
    
3. **Icons categorization:** We have published a private NPM package named `@pietra/icons` and created three workflows for icons: filled, outlined (where strokes are converted to fills in the outline paths), and colored (where all fill colors and gradients are preserved). We should categorize the icons in Figma the same way as in the code: place them in the filled, outlined, and colored frames, and replace `alternate` with `filled` or `outlined` in their names.
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749522808695/053ca964-72ef-4b61-9aeb-b10cbfec9a65.png align="center")
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749522856491/9666ca0b-b236-4d7c-8bbc-b1cf2513dca4.png align="center")
    
4. **Align the form components:** Currently, the form components in Figma, such as buttons, selects, and inputs, have different properties than those in the code. As a result, we have to customize these components repeatedly. We should align the design and code of these components once to avoid any more repeated overrides.
    

[![Screenshot of a component playground interface with a description field. It includes advice to limit campaigns to 30 days, as those over 60 days are rarely successful. Options for input type, size, and variable modes are on the right.](https://cdn.hashnode.com/res/hashnode/image/upload/v1749547998863/4f642afc-7c5b-4bed-aadd-4759a7b180b4.png align="center")](https://www.figma.com/design/ogjn6pRFttytQXQNP4g5Qb/%F0%9F%92%8E-Pietra-Design-System?node-id=1533-23876&t=2bHoBM0CzdxF2hEs-4)

Instead of building all the input components from scratch, we can simply copy them from the [Ant Design Open Source (Community) Figma](https://www.figma.com/community/file/831698976089873405).

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1749602805237/8fc9da9f-3ad1-41f0-9470-d72bd86e41e3.png align="center")

## A checklist for design review

Individual abilities are always limited, and no matter how hard you try, you might still miss some details without realizing it. So, before the design moves to the development stage, having colleagues review it can help reduce problems caused by accidentally overlooking something. Here is a checklist I recommend for the design review process:

1. How to measure the success of the feature and what’s the typical user flows?
    
2. Will these changes affect other pages or modules?
    
3. Should there be variations for different user types (such as different levels of paid subscriptions)?
    
4. Do these variations conflict with existing logic?
    
5. Are page-level containers frames with common device resolutions rather than casually sized sections?
    
6. Are all font sizes, border sizes, rounded corners, spacing, etc. directly referenced from predefined variables in the design system? Are they all integers?
    
7. How will the new design look on different devices, such as 2K and 4K screens, MacBook Air, MacBook Pro, tablets, and mobile phones?