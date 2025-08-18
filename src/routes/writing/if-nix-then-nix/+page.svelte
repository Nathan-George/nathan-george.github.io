<main>
	<article>
		<header>
			<h1>If Nix Then Nix</h1>
			<p>
				<time datetime="August 16, 2025">August 16, 2025</time>
			</p>
		</header>

		<p>
			This year, I decided to finally write my personal website where I publish my blog and host resources students can use to learn computer science. While writting one of the web pages, I was side tracked by the fact that the syntax highlighting for the CSS in my editor was not showing up. In most cases, the fix for this issue is adding a vscode extention or installing the treesitter parser, but I had no luck with either. The root of this particular issue was that I had installed treesitter through my editor's package manager instead of through nix which is not supported. It took me five hours to get my editor's package manager and nix to finally play nice with each other after struggling through nix's documentation. The general rule of thumb that I have found is that if you use nix then you should use nix to install and manage everything. Thus, the solution most nost nix users seem use for managing syntax highlighting are tools like Home Manager which allows users to add extentions to vscode in their nix configuration or NixVim for installing and configuring vim plugins. I believe the main reason for this is that NixOS is not FHS complient because it tries to ensure different versions of the same package don't mess with each other. Thus, software installed outside of nix encounters issues when it tries to look for or install binaries in these locations. While it may be posible to manage things like extentions, pluggins or other software outside of nix, eventually I have relized that the idiomatic nix way is the path of least resistance.
		</p>

		<p>
			It may be pretty obvious that if you use a package manage then you have to use said package manager, but there are reasons to desire not to. The primary one for me is that, as a TA for two CS classes, I want to be able to help students using other linux distributions, macOS, and Windows install and use software for class. Notably, using linux already makes me worse at this as most CS students use macOS or Windows, and my ability to help those students with getting their python interpreter setup is more limited. Now using a niche package manager which enforces the idiomatic nix way, I learn new tools like neovim in the nix way as opposed to a more standard way, and I expect this will make it more difficult for me to help other students interested in applications like neovim to learn how to configure them. That is to say I would rather configure something in the standard way as opposed to the nix way because I want my knowledge to be shareable. Another potential reason one might want to configure a program in a more standard way is that they already have some existing configuration or familiarity with a programs own builtin package manager which has its own ways of garrenteeing reproducability, but I find this reason more dubious as the nix interested user ought to have the expectation that they are learning a new piece of software which will certianly change how they set up their operating system.
		</p>

		<p>
			In some sense, I find NixOS to be a rather self-centered operating system in this way. It serves a user like me excelently with its reproducability, but it likes to pretend that users of other operating systems don't exist. For instance, it is common to add a nix flake to projects to setup a reproducable development environment, but for people who colaborate with me on these projects, these files are somewhat of an annoyance and are largely only there to tell other programmers, "I use NixOS." When writting additional configuration for a program, the idiomatic nix way has it setup in nix files instead of the program's own configuration language which makes porting a configuration with a non-nix user difficult.
		</p>

		<p>
			The second consequence of the "If Nix Then Nix" observation is that because nix is ought to be used to configure everything, then you must be able to find the documentation about how to use nix to configure it. Nix's documentation is sparse. I am hesitant to make this claim as I have often found that an observation of lacking documentation may be caused by not knowing what the right reference matterial is, but as it is I have not found it. Part of the reason I find searching for nix documentation so difficult is that I do not know nix well enough to search for the right thing. For instance, I searched for "How to convert text to a file" to figure out how to make additional config files for one application, but the answer to that question only puts that file in the nix store. Compared to looking up documentation for developing software, I have found looking up documentation for an operating system to be different different in that software documentation tends to be about how to a thing whereas OS documentation encompases more about settings, packages, and declaring config files. At the moment, I am less experianced at querying documentation for operating systems. In addition to this, NixOS has documentation for both an operating system and for a programming language. What this all means is that the piece of information I am looking for may be in any one of 4 places I have found or none at all.
		</p>

		<ul>
			<li>https://nix.dev/</li>
			<li>https://nix.dev/manual/nix/2.30/</li>
			<li>https://nixos.wiki/</li>
			<li>https://nixos.org/manual/nixos/stable/</li>
		</ul>

		<p>
			This reflection on nix as an operating system, has lead me to two conclutions. First, that newer or niche software has downsides for the person who values being able to help others with their own software or systems, as is the case in my need to help other students. The second is that we have not quite figured out documentation, in that I suspect most users of their computers likely expect the first result on google to answer their question as opposed to the more lengthy process of reading through a manual. This second observation is really why I still need to help students install software or understand some confusing syntax, because if we had good ways of communicating this information in our documentation then I would not need to help students. I suspect that AI may be able to help significantly in improving documentation as a search tool that can understand what a user is looking for better than other techniques, though this seems to still be a double edge sword where halucinations or asumptions made by the language model could steer the user off course.
		</p>
	</article>
</main>

<style>
	main {
		width: 800px;
		max-width: 95%;
		margin: 0 auto
	}

	header {
		margin: 0 0 2rem
	}

	header > h1 {
		font-size: 3em;
	}

	header > p {
		font-family: sans-serif;
	}

	article > p {
		margin: 0 0 40px;
		font-size: 24px;
		text-align: justify;
	}

	article > ul {
		margin: 0 40px 40px;
		font-size: 24px;
	}
</style>
