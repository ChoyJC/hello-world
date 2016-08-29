# hello-world
#import<Foundation/Foundation.h>
@interface JJ:NSObject
@end//JJ
@implementation JJ
-(NSString *)description
{
	return @"I am a 18cm JJ.";
}
@end

@interface Hand:NSObject
@end//Hand
@implementation Hand
-(NSString *)description
{
	return @"I am a hand.";
}
@end

@interface Leg:NSObject
@end
@implementation Leg
-(NSString *)description
{
	return @"I am a leg.";
}
@end

@interface Man:NSObject
{
	Leg *leg[2];
	Hand *hand[2];
	JJ *jj;
}
-(void)print;
@end;
@implementation Man
 -(id)init
{
	if(self==[super init])
	{
		leg[0]=[Leg new];
		leg[1]=[Leg new];
		hand[0]=[Hand new];
		hand[1]=[Hand new];
		jj=[JJ new];
	}
	return self;
}
-(void)print
{
	NSLog(@"%@",leg[0]);
	NSLog(@"%@",leg[1]);
	NSLog(@"%@",hand[0]);
	NSLog(@"%@",hand[1]);
	NSLog(@"%@",jj);
}
@end
int main(int argc, char const *argv[])
{
	Man *man;
	man=[Man new];
	[man print];
	return 0;
}











